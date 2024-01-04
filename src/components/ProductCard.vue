<script>
export default {
    name: 'ProductCard',
    props:{
        details: Object
    }
}
</script>
<template>
    <div class="col-2"><img :src="details.thumb" alt="">
    <h6>{{details.series}}</h6></div>
</template>
<style lang="scss" scoped>

@import '../styles/general.scss';
@import '../styles/partials/_variables';

.col-2{
    img{
        width: 150px;
        height: 150px;
       object-fit: cover;
       object-position: top;
    }
    h6{
        margin: 10px 0px;
    }
}
</style>