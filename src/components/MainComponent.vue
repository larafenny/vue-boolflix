<template>
    <main>
        <FilmList />
    </main>
</template>

<script>
import FilmList from './FilmList.vue'

export default {
    name: 'MainComponent',
    components:{
        FilmList,
    },
    props:{
        films: Array
    }
}
</script>

<style lang="scss">
    main{
        background-color: rgb(34, 33, 32);
        width: 100vw;
        height: calc(100vh - 60px);
        display: flex;
    }

</style>