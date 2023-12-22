<script>
export default {
    name: 'AppMainBlue',
    data(){
        return{
            list_info: [
                {
                    name: 'DIGITAL COMICS',
                    url_img: '../assets/img/buy-comics-digital-comics.png'
                },
                {
                    name: 'DC MERCHANDISE',
                    url_img: '../assets/img/buy-comics-merchandise.png'
                },
                {
                    name: 'SUBSCRIPTION',
                    url_img: '../assets/img/buy-comics-subscriptions.png'
                },
                {
                    name: 'COMIC SHOP LOCATOR',
                    url_img: '../assets/img/buy-comics-shop-locator.png'
                },
                {
                    name: 'DC POWER VISA',
                    url_img: '../assets/img/buy-dc-power-visa.svg'
                }
            ]
        }
    },
    methods:{
        getImagePath(imgPath){
            return new URL(imgPath,import.meta.url).href;
        }
    }
}
</script>
<template>
    <div class="blue_background">
        
        <div class="main-container">
            <ul class=" flex-container">
                <li v-for="element in list_info">
                    <div class="flex-container">
                        <img :src="getImagePath(element.url_img)" alt="">
                        <h6>{{element.name}}</h6>
                    </div>
                </li>
            </ul>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@import '../styles/general.scss';
@import '../styles/partials/_variables';


.main-container {
    height: 150px;
    // background-color: $black_background;
    h2{
        color: white;
        font-weight: lighter;
    }
}
.flex-container {
    justify-content: space-evenly;
    gap: 10px;
}
.blue_background{
    background-color: $blue_background;
}
ul{
    list-style: none;
    li{
        color: white;
        h6{
            font-weight: lighter;
        }
        img{
            width: 40px;
            // height: 50px;
        }
    }
}
</style>