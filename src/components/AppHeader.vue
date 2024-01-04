<script >
export default {
    name: 'AppHeader',
    data() {
        return {
            listPages: [
                {
                    name: 'CHARACTERS',
                    url: '#CHARACTERS',
                    active: false
                },
                {
                    name: 'COMICS',
                    url: '#COMICS',
                    active: true
                },
                {
                    name: 'MOVIES',
                    url: '#MOVIES',
                    active: false
                },
                {
                    name: 'TV',
                    url: '#TV',
                    active: false
                },
                {
                    name: 'GAMES',
                    url: '#GAMES',
                    active: false
                },
                {
                    name: 'COLLECTIBLES',
                    url: '#COLLECTIBLES',
                    active: false
                },
                {
                    name: 'VIDEOS',
                    url: '#VIDEOS',
                    active: false
                },
                {
                    name: 'FANS',
                    url: '#FANS',
                    active: false
                },
                {
                    name: 'NEWS',
                    url: '#NEWS',
                    active: false
                },
                {
                    name: 'SHOP',
                    url: '#SHOP',
                    active: false
                },


            ]
        }
    }
}


</script>

<template>
    <header >
        <div class="main-container">
            <div class="flex-container">
                <img src="../assets/img/dc-logo.png" alt="">
                <ul class="flex-container">
                    <li v-for="pages in listPages" :class="pages.active ? 'blu_active_border' : ''" >
                        <a :href="pages.url" class="black_a_color">{{pages.name}}</a>
                    </li>
                </ul>
            </div>
        </div>
    </header>
</template>

<style  scoped lang="scss">

@import '../styles/general.scss';
@import '../styles/partials/_variables';
header{
    padding: 2rem;
    background-color: white;
    img{
            width: 80px;
        }
}
ul{
    list-style-type: none;
    li{
        // padding: 0.8rem;
        a{
            color: $colore;
            padding: 0.8rem;
            // border-bottom: 1px solid $blu_active_border;
           
        }
        
       
    }
}

</style>
