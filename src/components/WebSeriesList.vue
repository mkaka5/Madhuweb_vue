<template>
    <div>
        <div v-for="series of webSeriesData" :key="series.series_id" >
            <WebSeries :series= series />
        </div>
    </div>
</template>

<script>
    import WebSeries from "./WebSeries.vue";
    
    export default{
        name: 'WebSeriesList',
        components: {
            WebSeries
        },
        props:{  
            webSeriesData: Array
        }
    }
</script>

<style scoped>

</style>