<script>
export default {
    name: 'ImageCollage',
}
</script>

<template>
    <div class="image-container d-flex ">
        <p class="oswald-medium text-uppercase">go ahead and<br>build your<br>own pizza<br>we won't<br>judge!</p>
        <div class="left-group d-flex flex-column">
            <div class="top-image"></div>
            <div class="center-image"></div>
            <div class="bottom-image"></div>
        </div>

        <div class="center-group d-flex flex-column">
            <div class="top-image"></div>
            <div class="center-image"></div>
            <div class="bottom-image"></div>
        </div>

        <div class="right-group d-flex flex-column">
            <div class="top-image"></div>
            <div class="center-image"></div>
            <div class="bottom-image"></div>
        </div>

    </div>



</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

.image-container {
    margin-bottom: $smallMargin;
    position: relative;

    p {
        position: absolute;
        top: 50%;
        left: 20%;
        transform: translateY(-50%);

        font-size: 4em;
        line-height: 1em;
        color: white;

    }

    .left-group {
        width: 10%;

        .top-image {
            width: 100%;
            height: 135px;
            background-image: url('/img/h3-background-img.jpg');
            background-position: bottom right;
        }

        .center-image {
            width: 100%;
            height: 295px;
            background-image: url('/img/h3-background-img.jpg');
            background-position: top right;
        }

        .bottom-image {
            width: 100%;
            height: 135px;
            background-image: url('/img/h3-background-img.jpg');
            background-position: center right;
        }
    }

    .center-group {
        width: 100%;

        .top-image {
            width: 100%;
            height: 135px;
            background-image: url('/img/h3-background-img.jpg');
            background-position: bottom;
        }

        .center-image {
            width: 100%;
            height: 295px;
            background-image: url('/img/h3-background-img.jpg');
            background-position: top;
        }

        .bottom-image {
            width: 100%;
            height: 135px;
            background-image: url('/img/h3-background-img.jpg');
            background-position: center;
        }
    }

    .right-group {
        width: 10%;

        .top-image {
            width: 100%;
            height: 135px;
            background-image: url('/img/h3-background-img.jpg');
            background-position: bottom left;
        }

        .center-image {
            width: 100%;
            height: 295px;
            background-image: url('/img/h3-background-img.jpg');
            background-position: top left;
        }

        .bottom-image {
            width: 100%;
            height: 135px;
            background-image: url('/img/h3-background-img.jpg');
            background-position: center left;
        }
    }

}
</style>