<template>
    <div class="topHeader">
        <div class="logo">
            <img src="../assets/Netflix-logo.png" alt="logo">
        </div>
        
        <div class="menu">
            <div class="searchbar">
                <input type="text" class="search" 
                    @keyup.enter="cerca"
                    placeholder="Cerca">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HeaderComponent',

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
            margin-right: 20px;
            .search{
                width: 100%;
            }
            
        }
    }
    }
    
</style>