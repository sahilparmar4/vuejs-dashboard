<template>
    <canvas ref="barChart"></canvas>
</template>

<script>
    import Chart from "chart.js/auto";

    export default {
    name: 'BarChart',
    mounted(){
        const ctxForBar = this.$refs.barChart.getContext('2d');
        const myBarChart  = new Chart(ctxForBar, {
            type: 'bar',
            data: {
            labels: ['BJP', 'INC', 'BSP', 'SP', 'TMC', 'AAP'],
            datasets: [{
                label: 'Election Results',
                data: [12, 19, 3, 5, 2, 3],
                borderWidth: 1,
                backgroundColor: ["#ff6600", "#00ffcc", "#ccffff", "#0033cc", "#00ff00", "#000000"]
            }]
            },
            options: {
                scales: {
                    y: {
                        beginAtZero: true
                    }
                }
            }
        });

        myBarChart;
    }
    }
</script>
