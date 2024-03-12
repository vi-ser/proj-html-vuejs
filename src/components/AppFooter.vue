<script>

import { store } from '../store';
import RestaurantItem from '../components/RestaurantItem.vue'
import HoursItem from '../components/HoursItem.vue';

export default {
    name: 'AppFooter',

    data() {
        return {
            store,
        }
    },

    components: {
        RestaurantItem,
        HoursItem,
    }
}
</script>

<template>
    <footer class="d-flex">
        <div class="footer-left d-flex justify-content-between">
            <div class="left-container">
                <h6 class="text-uppercase oswald-medium">find our restaurants</h6>
                <ul class="list-unstyled">
                    <RestaurantItem v-for="currentRestaurant in store.restaurant" :restaurant="currentRestaurant">
                    </RestaurantItem>
                </ul>
            </div>
            <div class="center-container">
                <h6 class="text-uppercase oswald-medium">working hours</h6>

                <ul class="list-unstyled mb-3">
                    <HoursItem v-for="currentHour in store.hour" :hour="currentHour"></HoursItem>
                </ul>

                <div class="social d-flex gap-2 align-items-center">
                    <span class="follow-us oswald-medium text-uppercase">follow us:</span>
                    <i class="fa-brands fa-x-twitter"></i>
                    <i class="fa-brands fa-facebook-f"></i>
                    <i class="fa-brands fa-instagram"></i>
                    <i class="fa-brands fa-linkedin-in"></i>
                </div>
            </div>
            <div class="right-container">
                <span class="text-uppercase text-white oswald-medium fs-4">the don peppe crew<br>first and
                    foremost<br>values
                    an authentic,<br>well baked slice of<br>pizza.</span>
            </div>
            <img class="footer-logo" src="/img/footer-bottom-img.png" alt="">
        </div>
        <div class="footer-right">
        </div>
    </footer>


</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

footer {

    height: 640px;

    .footer-left {
        width: 50%;
        background-image: url('/img/cielostellato.PNG');
        padding: 125px 100px 35px 50px;
        position: relative;

        h6 {
            color: $accent;
            margin-bottom: 20px;
        }

        .follow-us {
            color: $accent;
            font-size: .8em;
        }

        i {
            color: white;
            font-size: .8em;
            cursor: pointer;
        }

        .footer-logo {
            position: absolute;
            bottom: 35px;
            right: 55px;
        }
    }

    .footer-right {
        width: 50%;
        background-image: url('/img/footer-img-1.jpg');
        background-size: cover;
        background-position: center;
    }
}
</style>