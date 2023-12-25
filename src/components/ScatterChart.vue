<template>
    <canvas ref="scatterChart"></canvas>
</template>

<script>
    import Chart from "chart.js/auto";
    export default {
        
        name: "ScatterChart",
        mounted(){
            const ctxForScatter = this.$refs.scatterChart.getContext("2d");

            const myScatterChart = new Chart(ctxForScatter, {
                type: 'scatter',
                data:{
                    datasets: [{
                        label: 'Scatter Plot',
                        data: [{
                        x: -10,
                        y: 0
                        }, {
                        x: 0,
                        y: 10
                        }, {
                        x: 10,
                        y: 5
                        }, {
                        x: 0.5,
                        y: 5.5
                        },
                        {
                            x:4,
                            y: 12
                        },
                        {
                            x: 7,
                            y: 7
                        },
                        {
                            x: 13,
                            y: 7
                        },
                        {
                            x: 5,
                            y: 11
                        },
                        {
                            x: 30,
                            y: 4
                        }
                    ],
                        backgroundColor: 'rgb(255, 99, 132)'
                    }],
                }
            });

            myScatterChart;
        }
    }
</script>