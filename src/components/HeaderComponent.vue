<template>
    <div class="topHeader">
        <div class="logo">
            <img src="../assets/Netflix-logo.png" alt="logo">
        </div>
        
        <div class="menu">
            <div class="searchbar">
                <input type="text" class="search" 
                    v-model="searchFilm"
                    @keyup.enter="search"
                    placeholder="Cerca">
                    <button class="search-button" 
                    @click="search">Cerca</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HeaderComponent',
    data(){
        return{
            searchFilm:''
        }
    },
    methods:{
        search(){
            this.$emit('search', this.searchFilm)
        }
    }

}
</script>

<style lang="scss">
    .topHeader{
        display: flex;
        align-items: center;
        background-color: #302e2e;
        height: 60px;

        .logo{
        width: 10%;
        img{
            max-width: 100%;
            padding: 0 10px;
        }
    }
    .menu{
        width: 90%;
        display: flex;
        justify-content: flex-end;
        .searchbar{
            width: 25%;
            margin-right: 30px;
            display: flex;
            .search{
                width: 80%;
                margin-right: 5px;
                border-radius: 3px;
            }
            button{
                width: 20%;
                border-radius: 3px;

            }
            
        }
    }
    }
    
</style>