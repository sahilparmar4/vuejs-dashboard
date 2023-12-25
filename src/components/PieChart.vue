<template>
    <canvas ref="pieChart"></canvas>
</template>

<script>
    import Chart from "chart.js/auto";

    export default{
        name: "PieChart",
        mounted(){
            const ctxForPie = this.$refs.pieChart.getContext("2d");

            const myPieChart = new Chart(ctxForPie,{
                type: "pie",
                data:{
                    labels: [
                        'Uttar Pradesh',
                        'Maharashtra',
                        'Bihar',
                        "West Bengal",
                        "Madhya Pradesh",
                        "Others"
                    ],
                    datasets: [{
                        label: 'Population of Indian States',
                        data: [21.2, 10.8, 11.2, 9.5, 7.5, 39.8],
                        backgroundColor: [
                        'rgb(255, 99, 132)',
                        'rgb(54, 162, 235)',
                        'rgb(255, 205, 86)',
                        "rgb(255, 204, 153)",
                        "rgb(153, 51, 255)",
                        "rgb(255, 153, 204)"
                        ],
                        hoverOffset: 4
                    }]
                },
                options:{
                    responsive: true,
                    plugins:{
                        title:{
                            display: true,
                            text: "Population of India"
                        }
                    }
                }
            });

            myPieChart;
        }
        
    }
</script>