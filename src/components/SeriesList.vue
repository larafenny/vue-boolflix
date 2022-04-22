<template>
    <div>
        <h1>SERIES</h1>
        <div class="container">
            <div class="row">
                <div class="card" v-for="series in series" :key="series.id ">
                    <h1>{{series.name}}</h1>
                    <h2>{{series.original_title}}</h2>
                    <h3>{{series.original_language}}</h3>
                    <h4>{{series.vote_average}}</h4>
                </div>

            </div>
        </div>
    </div>


</template>

<script>
export default {
    name: 'SeriesList',
    props: {
        series: Array
    }

}

/*
backdrop_path: (…)
first_air_date: (…)
genre_ids: (…)
id: (…)
name: (…)
origin_country: (…)
original_language: (…)
original_name: (…)
overview: (…)
popularity: (…)
poster_path: (…)
vote_average: (…)
vote_count: (…)
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

