<template>
    <main>

    </main>
</template>

<script>
export default {
    name: 'MainComponent',
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