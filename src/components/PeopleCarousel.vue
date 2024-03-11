<script>
export default {
    name: 'PeopleCarousel',

}
</script>

<template>
    <div id="carousel" class="d-flex">
        <img src="/img/h1-team-1a-700x700.jpg" alt="">
        <img src="/img/h1-team-2a.jpg" alt="">
        <img src="/img/h1-team-3a.jpg" alt="">
        <img src="/img/h1-team-4a.jpg" alt="">
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

#carousel {
    margin-bottom: $smallMargin;

    img {
        width: calc(100% / 4);
        height: 100%;
    }
}
</style>