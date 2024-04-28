<template>
    <div class="series-container">
        <div class="series-image">
            <img :src=series.series_image alt=series.series_mylist class="image">
        </div>
        <div class="series-details">
            <h1>{{series.series_myList}}</h1>
            <h2> Recently added : {{series.series_recentlyadded}}</h2>
            <p> Trending: {{series.series_trending}}</p>
            <p class="genre"> {{series.series_genre}}</p>
            <p> Top Searches : {{series.series_topSearches}}</p>
            <p> Downloads : {{series.series_downloads}}</p>
        </div>
    </div>
</template>

<script>

export default{
    name: 'WebSeries',
    props:{
        series: Object
    }
}
</script>

<style scoped>
    .series-container{
        display: grid;
        grid-template-columns: 0.5fr 1fr;
        row-gap: 2opx;
        width:80%;
        margin: 1em auto;
        border:transparent;
        border-radius: 10px;
        box-shadow:0 4px 8px 0 rgba(0,0,0,0.2),0 6px 20px 0 rgba(0,0,0,0.19);
        padding: 1em;
    }
    .genre{
        border: 1px solid #669bbc;
        border-radius: 5px;
        padding: 0.5em;
        display: inline;
        background: #669bbc;
        color:white;
    }
    .series-image .image{
        width: 350px;
        height: 300px;
    }

</style>
