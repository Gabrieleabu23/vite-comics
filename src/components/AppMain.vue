<script>
export default {
    name: 'AppMain'
}
</script>
<template>
    <div class="black_background">
        
        <div class="main-container flex-container">
            <h2>&rightarrow; Content goes here &LeftArrow; </h2>
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
.black_background{
    background-color: $black_background;
}
</style>