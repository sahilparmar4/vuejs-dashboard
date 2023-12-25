<template>
    <canvas ref="doughnutChart"></canvas>
</template>

<script>
    import Chart from "chart.js/auto";
    export default{
        name: "DoughnutChart",
        mounted(){
            const ctxForDoughnut = this.$refs.doughnutChart.getContext('2d');
            const myDoughnutChart = new Chart(ctxForDoughnut,{
                type: 'doughnut',
                data:{
                    labels: [
                        'Others',
                        'Mumbai Indians',
                        'Chennai Super Kings'
                    ],
                    datasets: [{
                        label: 'IPL Trophies won',
                        data: [5, 5, 5],
                        backgroundColor: [
                        'rgb(255, 99, 132)',
                        'rgb(54, 162, 235)',
                        'rgb(255, 205, 86)'
                        ],
                        hoverOffset: 4
                    }]
                },
                options:{
                    responsive: true,
                    plugins:{
                        title:{
                            display: true,
                            text: "IPL Trophies"
                        }
                    }
                }
            });
            myDoughnutChart;
        }
    }
</script>