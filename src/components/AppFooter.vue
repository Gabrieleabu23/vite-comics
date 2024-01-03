<script>
export default {
    name: 'AppFooter',
    data() {
        return {
            indice: 0,
            scambioinfo: "",
            vettorescambio: [],
            list_info: [
                {
                    name: 'DC COMICS',
                    info_array: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News']
                },
                {
                    name: 'DC ',
                    info_array: ['Terms Of Use', 'Provacy policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Rating', 'Shop Help', 'Contact Us']
                },
                {
                    name: 'SITES',
                    info_array: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
                },
                {
                    name: 'SHOP',
                    info_array: ['Shop DC', 'Shop DC Collectibles']
                }
            ],
            social_list: [
                {
                    name: "#FACEBOOK",
                    url_img: '../assets/img/footer-facebook.png'
                },
                {
                    name: "#TWITTER",
                    url_img: '../assets/img/footer-twitter.png'
                },
                {
                    name: "#YOUTUBE",
                    url_img: '../assets/img/footer-youtube.png'
                },
                {
                    name: "#PINTEREST",
                    url_img: '../assets/img/footer-pinterest.png'
                },
                {
                    name: "#PERISCOPE",
                    url_img: '../assets/img/footer-periscope.png'
                }
            ]
        }
    },
    methods: {
        ottieniLink() {

            // DEBUG
            // console.log(this.list_info.length);
            while (this.indice <= this.list_info.length) {

                for (const item of this.list_info) {
                    if (item.info_array) {
                        this.vettorescambio.push(item.info_array.join(' '));
                    }
                }
                this.indice++;


            }

        },
        getImagePath(imgPath){
            return new URL(imgPath,import.meta.url).href;
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
            <ul class="col-5 flex-container">
                <div v-for="(item, index) in list_info" :key="index" class="col-4">
                    <h3>{{ item.name }}</h3>
                    <li v-for="(info, infoIndex) in item.info_array" :key="infoIndex">
                        <a>{{ info }}</a>
                    </li>
                </div>
            </ul>
        </div>
        <div class="social-container-bg">
            <div class="main-container">
                <div class="flex-container">
                    <a href="#" class="col-5">SIGN UP NOW!</a>
                    <div class=" flex-container gap-ul-container">
                        <h4>FOLLOW US!</h4>
                        <ul class="flex-container">
                            <li v-for="element in social_list">
                                   <a :href=element.name><img :src="getImagePath(element.url_img)"></a>  
                                    
                            </li>
                        </ul>
                    </div>
                </div>
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

ul {
    list-style: none;

    li {
        font-size: 12px;
        font-weight: lighter;

        a {
            color: $grey_text_link;
            cursor: pointer;
            font-weight: lighter;
            font-size: 0.7rem;
        }
    }
}

a.col-5 {
    margin-left: 20px;
    border: 1px solid $blue_border_button;
    color: white;
    text-align: center;
    font-size: 15px;
    padding: 15px 5px;
    width: 150px;
}

.flex-container {
    flex-wrap: wrap;
}

.col-5.flex-container {
    align-items: stretch;
}

.col-4 {
    margin-top: 20px;
}

.col-5 {
    padding: 20px;
}

.col-3,
h3 {
    color: white;
    font-weight: lighter;
}

.social-container-bg {
    width: 100%;
    padding-bottom: 10px;
    height: calc($height_container + 20px);
    background-color: $grey_background_color;

    h4 {
        font-weight: lighter;
        color: $blue_border_button;
        font-size: 20px;
    }
    .gap-ul-container{
        gap: 30px;
    }
    ul{
        gap: 20px;
    }
}</style>