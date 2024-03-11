<script>
export default {
    name: 'PartnersItem',
}
</script>

<template>
    <div id="partners" class="d-flex justify-content-center">
        <div class="logo-container">
            <img src="/img/h1-clients-img-4.png" alt="">
        </div>
        <div class="logo-container">
            <img src="/img/h1-clients-img-3.png" alt="">
        </div>
        <div class="logo-container">
            <img src="/img/h1-clients-img-1.png" alt="">
        </div>
        <div class="logo-container">
            <img src="/img/h1-clients-img-2.png" alt="">
        </div>
        <div class="logo-container">
            <img src="/img/h1-clients-img-5.png" alt="">
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

#partners {
    background-color: $bgLight;
    padding: 80px 0;

    .logo-container {
        display: flex;
        justify-content: center;
        align-items: center;

        img {
            height: 80%;
        }
    }
}
</style>