<script>
export default {
    name: 'JumboCarousel',

}
</script>

<template>
    <div id="carousel" class="d-flex">
        <div class="image-card">
            <div class="front-card">
                <img src="/img/h3-img-1.jpg" alt="">
            </div>
            <div class="back-card">
                <i class="fa-regular fa-eye"></i>
            </div>
        </div>
        <div class="image-card">
            <div class="front-card">
                <img src="/img/h3-img-2.jpg" alt="">
            </div>
            <div class="back-card">
                <i class="fa-regular fa-eye"></i>
            </div>
        </div>
        <div class="image-card">
            <div class="front-card">
                <img src="/img/h3-img-3.jpg" alt="">
            </div>
            <div class="back-card">
                <i class="fa-regular fa-eye"></i>
            </div>
        </div>
        <div class="image-card">
            <div class="front-card">
                <img src="/img/h3-img-4.jpg" alt="">
            </div>
            <div class="back-card">
                <i class="fa-regular fa-eye"></i>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

#carousel {
    padding: $smallMargin 0;
    gap: $smallMargin;

    background-color: white;

    .image-card {
        position: relative;
        width: calc(100% / 4 - $smallMargin / 4 * 3);



        img {
            width: 100%;
        }

        .back-card {
            position: absolute;
            top: 0;
            left: 0;

            display: none;
            justify-content: center;
            align-items: center;

            width: 100%;
            height: 100%;

            background-image: url('/img/pattern.png');


            i {
                color: white;
                background-color: $primary;
                padding: 20px;
                border-radius: 50%;
                cursor: pointer;
            }

        }

        &:hover .back-card {
            display: flex;
        }
    }
}
</style>