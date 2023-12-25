<template>
    <h1>Dashboard</h1>
        <div class="row">
            <div class="col-lg-4 col-md-6 col-sm-1">
                <BarChart />
            </div>
            <div class="col-lg-4 col-md-6 col-sm-1">
                <LineChart />
            </div>
            <div class="col-lg-4 col-md-6 col-sm-1">
                <ScatterChart />
            </div>
            
            <div class="col-lg-4 col-md-6 col-sm-1">
                <DoughnutChart />
            </div>
            <div class="col-lg-4 col-md-6 col-sm-1">
                <RadarChart />
            </div>
            <div class="col-lg-4 col-md-6 col-sm-1">
                <PieChart />
            </div>
        </div>
       
</template>

<script>
    
    import BarChart from "./BarChart.vue";
    import LineChart from "./LineChart.vue";
    import ScatterChart from "./ScatterChart.vue"
    import DoughnutChart from "./DoughnutChart.vue";
    import RadarChart from "./RadarChart.vue";
    import PieChart from "./PieChart.vue";

    export default {
        name: "VisualizationDashboard",
        components:{
            BarChart,
            LineChart,
            ScatterChart,
            DoughnutChart,
            RadarChart,
            PieChart
        },
        
    }
</script>

<style>
   
</style>