<template>
    <main>
        <FilmList :films="films"/>
        <SeriesList :series="series" />
    </main>
</template>

<script>
import FilmList from './FilmList.vue'
import SeriesList from './SeriesList.vue'

export default {
    name: 'MainComponent',
    components:{
        FilmList,
        SeriesList
    },
    props:{
        films: Array,
        series: Array
    }
}
</script>

<style lang="scss">
    main{
        background-color: rgb(34, 33, 32);
        width: 100vw;
        height: calc(100vh - 60px);
        overflow: scroll;
    }

</style>