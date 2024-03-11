<script>

import NavItem from '../components/NavItem.vue'
export default {
    name: 'AppHeader',

    components: {
        NavItem,
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
</template>

<style lang="scss" scoped>
.header {
    background-image: url('/img/cielostellato.PNG');
    height: 610px;

    .img-container {
        height: 400px;
        position: relative;

        .jumbo-img {
            height: 100%;
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