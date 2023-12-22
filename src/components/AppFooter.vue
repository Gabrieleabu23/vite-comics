<script>
export default {
    name: 'AppFooter',
    data() {
        return {
            vettorescambio: [],
            list_info: [
                {
                    name: 'DC COMICS',
                    info_array: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News']
                },
                {
                    name: 'DC ',
                    info_array: ['Terms Of Use', 'Provacy policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops','CPSC Certificates','Rating','Shop Help','Contact Us']
                },
                {
                    name: 'SITES',
                    url_img: '../assets/img/buy-comics-subscriptions.png'
                },
                {
                    name: 'SHOP',
                    url_img: '../assets/img/buy-comics-shop-locator.png'
                }
            ]
        }
    },
    methods: {
        ottieniLink() {
            this.list_info.forEach((element,i) => {
                let variabilescambio = element.info_array;
                if (variabilescambio) {
                    variabilescambio.forEach(subElement => {
                        this.vettorescambio.push(subElement)
                    });
                }
            });
        }
    },
    mounted() {
        this.ottieniLink();


    }
}
</script>
<template>
    <div class="image_background">
        <div class="main-container">
            <div class="col-5 flex-container">
                <ul v-for="element,i in list_info " :key="i" class="col-4">
                    <h3>{{element.name}}</h3>
                    <li v-for="indice,index in vettorescambio  " :key="index">
                    <a href="#">{{vettorescambio[index]}}</a></li>
                </ul>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@import '../styles/general.scss';
@import '../styles/partials/_variables';


.image_background {
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    // height: 300px;
    margin-bottom: 40px;
}
ul{
    list-style: none;
    li{
        a{
            color:$grey_text_link;
            font-weight: lighter;
            font-size: 0.7rem;
        }
    }
}
.flex-container{
    flex-wrap: wrap;
}
.col-4{
    margin-top:20px;
}
.col-5{
    padding: 20px;
}

.col-3,
h3{
    color: white;
    font-weight: lighter;
}
</style>