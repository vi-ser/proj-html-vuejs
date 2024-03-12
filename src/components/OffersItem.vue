<script>
export default {
    name: 'OffersItem',
}
</script>

<template>
    <div class="offers d-flex">
        <div class="left d-flex justify-content-center align-items-center">
            <img src="/img/h1-img-7n.png" alt="">
        </div>
        <div class="right d-flex align-items-center justify-content-center">
            <div class="offers-container">

                <h2 class="text-uppercase oswald-medium">
                    specials*
                </h2>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesent ut!</p>
                <div class="menu d-flex">
                    <span class="price oswald-medium">$10</span>
                    <div class="offer-item">
                        <span class="offer text-uppercase oswald-medium">combo
                            piccolo</span>
                        <p class="item-descr">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesent ut
                            aliquam
                            dui</p>
                    </div>
                </div>
                <div class="menu d-flex">
                    <span class="price oswald-medium">$20</span>
                    <div class="offer-item">
                        <span class="offer text-uppercase oswald-medium">combo
                            medio</span>
                        <p class="item-descr">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesent ut
                            aliquam
                            dui</p>
                    </div>
                </div>
                <div class="menu d-flex">
                    <span class="price oswald-medium">$30</span>
                    <div class="offer-item">
                        <span class="offer text-uppercase oswald-medium">combo
                            grande</span>
                        <p class="item-descr">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesent ut
                            aliquam
                            dui</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

.offers {

    margin-bottom: $smallMargin;

    .left {
        width: 50%;
        height: 750px;
        background-image: url('/img/h1-img-4.jpg');
        background-size: cover;
        background-position: center;

        img {
            width: 370px;
        }
    }

    .right {
        width: 50%;
        background-color: white;
        padding: 0 50px;
        color: $text;

        h2 {
            font-size: 2em;
            margin-bottom: 25px;
            padding: 0;
        }

        p {
            margin-bottom: 35px;
            color: $textLight;
        }

        .price {
            color: $primaryDark;
            margin-right: 10px;
            margin-bottom: 15px;
            font-size: 1.2em;
        }

        .offer-item {
            .offer {
                font-size: 1.2em;
            }

            .item-descr {
                font-size: .8em;
            }
        }
    }


}
</style>