<script >
export default {
    name: 'AppHeader',
    data() {
        return {
            listPages: [
                {
                    name: 'CHARACTERS',
                    url: '#CHARACTERS'
                },
                {
                    name: 'COMICS',
                    url: '#COMICS'
                },
                {
                    name: 'MOVIES',
                    url: '#MOVIES'
                },
                {
                    name: 'TV',
                    url: '#TV'
                },
                {
                    name: 'GAMES',
                    url: '#GAMES'
                },
                {
                    name: 'COLLECTIBLES',
                    url: '#COLLECTIBLES'
                },
                {
                    name: 'VIDEOS',
                    url: '#VIDEOS'
                },
                {
                    name: 'FANS',
                    url: '#FANS'
                },
                {
                    name: 'NEWS',
                    url: '#NEWS'
                },
                {
                    name: 'SHOP',
                    url: '#SHOP'
                },


            ]
        }
    }
}


</script>

<template>
    <header class="$hei">
        <div class="main-container">
            <div class="flex-container">
                <img src="../assets/img/dc-logo.png" alt="">
                <ul class="flex-container">
                    <li v-for="pages in listPages">
                        <a :href="pages.url" class="black_a_color">{{pages.name}}</a>
                    </li>
                </ul>
            </div>
        </div>
    </header>
</template>

<style  scoped lang="scss">

@use './styles/partials/_variables.scss' as *;
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
        padding: 0.8rem;
        a{
            color: $boh;
        }
    }
}

</style>
