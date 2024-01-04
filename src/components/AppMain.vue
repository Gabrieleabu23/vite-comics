<script>
import ListProducts from './ListProducts.vue'
export default {
    name: 'AppMain',
    components:{
        ListProducts
    }
}
</script>
<template>
    <div class="jumbo">
        <div class="main-container">
            <div class="current_series_comics">
                <h4>CURRENT SERIES</h4>
            </div>
        </div>
    </div>
    <div class="black_background">
        <div class="main-container flex-container">
            <ListProducts/>
        </div>
        <div class="flex-container center">
            <a href="#load more" class="button_blue">LOAD MORE</a>
        </div>
    </div>
        
</template>
<style lang="scss" scoped>
@import '../styles/general.scss';
@import '../styles/partials/_variables';

.main-container {
    height: $height_container;
    // background-color: $black_background;
    h2{
        color: white;
        font-weight: lighter;
    }
}
.jumbo{
    // DEBUG INIZIALE ESERCIZIO BASE
    // background-color: $black_background;
    background-image: url(../assets/img/jumbotron.jpg);
    background-size: cover;
    height: 400px;
    .main-container{
        height: 100%;
        position: relative;
    }
}
.black_background{
    margin-bottom: 20px;
    .main-container{
        width: 65%;
        margin: 30px auto;
        height: 100%;
    }
    .flex-container{
        flex-wrap: wrap;
    }
}
.current_series_comics{
    position: absolute;
    bottom: -20px;
    left: 60px;
    background-color: $blue_background;
    padding:10px 20px;
    // DEBUG
    // border: 1px solid black;
}

.button_blue{
    font-size: 12px;
    padding: 10px 50px ;
    color: white;
    background-color: $blue_background;
}
</style>