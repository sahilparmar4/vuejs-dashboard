<template>
    <canvas ref="radarChart"></canvas>
</template>

<script>
    import Chart from "chart.js/auto";

    export default {
        name: "RadarChart",
        mounted(){
            const ctxForRadarChart = this.$refs.radarChart.getContext("2d");
            const myRadarChart = new Chart(ctxForRadarChart, {
                type:"radar",
                data:{
                    labels: [
                        'Eating',
                        'Drinking',
                        'Sleeping',
                        'Designing',
                        'Coding',
                        'Cycling',
                        'Running'
                    ],
                     datasets: [{
                        label: 'Excercise',
                        data: [65, 59, 90, 81, 56, 55, 40],
                        fill: true,
                        backgroundColor: 'rgba(54, 162, 235, 0.2)',
                        borderColor: 'rgb(255, 99, 132)',
                        pointBackgroundColor: 'rgb(255, 99, 132)',
                        pointBorderColor: '#fff',
                        pointHoverBackgroundColor: '#fff',
                        pointHoverBorderColor: 'rgb(255, 99, 132)'
                    },
                    {
                        label: 'Excercise',
                        data: [64, 84, 51, 69, 42, 64, 75],
                        fill: true,
                        backgroundColor: 'rgba(255, 99, 132, 0.2)',
                        borderColor: 'rgb(255, 99, 132)',
                        pointBackgroundColor: 'rgb(255, 99, 132)',
                        pointBorderColor: '#fff',
                        pointHoverBackgroundColor: '#fff',
                        pointHoverBorderColor: 'rgb(255, 99, 132)'
                    },
                    {
                        label: 'Excercise',
                        data: [28, 40, 19, 96, 27, 100],
                        fill: true,
                        backgroundColor: 'rgba(54, 162, 235, 0.2)',
                        borderColor: 'rgb(54, 162, 235)',
                        pointBackgroundColor: 'rgb(54, 162, 235)',
                        pointBorderColor: '#fff',
                        pointHoverBackgroundColor: '#fff',
                        pointHoverBorderColor: 'rgb(54, 162, 235)'
                    }
                    ]
                },
                options:{
                    responsive: true,
                    plugins:{
                        title:{
                            display: true,
                            text: "Excercise & Daily Activities"
                        }
                    }
                }
            });
            myRadarChart;
        }
    }
</script>