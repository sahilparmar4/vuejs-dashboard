<template>
    <canvas ref="lineChart"></canvas>
</template>

<script>
    import Chart from "chart.js/auto";
    export default{
        name: "LineChart",
        mounted(){
            const ctxForLine = this.$refs.lineChart.getContext("2d");

            const myLineChart = new Chart(ctxForLine, {
                type: "line",
                data:{
                    labels: [2013, 2014, 2015, 2016, 2017, 2018, 2019, 2020, 2021, 2022, 2023],
                    datasets: [{
                        label: 'Mohammed Shami wickets over the years',
                        data: [47, 67, 25, 32, 23, 50, 78, 19, 29, 23, 56],
                        fill: false,
                        borderColor: 'rgb(75, 192, 192)',
                        tension: 0.1
                    }]
                }
            });

            myLineChart;
        }
    }
</script>