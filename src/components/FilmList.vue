<template>
    <div>
        <h1>FILM</h1>
        <div class="container">
            <div class="row">
                <div class="card" v-for="film in films" :key="film.id ">
                    <h1>{{film.title}}</h1>
                    <h2>{{film.original_title}}</h2>
                    <h3>{{film.original_language}}</h3>
                    <h4>{{film.vote_average}}</h4>
                </div>

            </div>
        </div>
    </div>


</template>

<script>
export default {
    name: 'FilmList',
    props: {
        films: Array
    }

}


/*
id: (…)
original_language: (…)
original_title: (…)
title: (…)
vote_average: (…)
*/
</script>

<style lang="scss" scoped>
    .container{
        color: rgb(124, 124, 124);
        .row{
            display: flex;
            flex-wrap: wrap;
            .card{
                width: calc(100% / 6 - 10px);
                border: solid 1px black;
                margin: 5px;
                display: flex;
                flex-direction: column;
                justify-content: space-evenly;
                padding: 0px 15px;
                h1{
                    font-size: 18px;
                }
                h2{
                    font-size: 16px;
                    
                }
                h3{
                    font-size: 14px;
                    text-align: right;
                }
                h4{
                    font-size: 12px;
                    text-align: right;
                    align-self: flex-end;

                }
            }

        }
    }
</style>>

