<script>

import NavItem from '../components/NavItem.vue'
import JumboCarousel from '../components/JumboCarousel.vue'
import JumboQuotes from '../components/JumboQuotes.vue'


export default {
    name: 'AppHeader',

    components: {
        NavItem,
        JumboCarousel,
        JumboQuotes,
    },
}
</script>

<template>
    <div class="header">
        <NavItem>
        </NavItem>
        <div class="img-container d-flex justify-content-center align-items-center">
            <img class="jumbo-img" src="/img/h3-rev-img-6.png" alt="">
            <img class="text-bg" src="/img/h3-rev-img-5.png" alt="">
        </div>
    </div>
    <JumboCarousel>
    </JumboCarousel>
    <JumboQuotes></JumboQuotes>
</template>

<style lang="scss" scoped>
.header {
    background-image: url('/img/cielostellato.PNG');
    /* height: 610px; */

    .img-container {
        position: relative;
        padding-bottom: 60px;


        .jumbo-img {
            height: 400px;
            z-index: 1;
        }

        .text-bg {
            position: absolute;
            height: 320px;
            bottom: 100px;

        }
    }
}
</style>