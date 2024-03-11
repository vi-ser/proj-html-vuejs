<script>
export default {
    name: 'JumboCarousel',

}
</script>

<template>
    <div id="carousel" class="d-flex">
        <img src="/img/h3-img-1.jpg" alt="">
        <img src="/img/h3-img-2.jpg" alt="">
        <img src="/img/h3-img-3.jpg" alt="">
        <img src="/img/h3-img-4.jpg" alt="">
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

#carousel {
    padding: $smallMargin 0;
    gap: $smallMargin;

    background-color: white;

    img {
        width: calc(100% / 4 - $smallMargin / 4 * 3);
        height: 100%;
    }
}
</style>