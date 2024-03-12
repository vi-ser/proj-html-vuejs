<script>
import { store } from '../store';
import NavLink from '../components/NavLink.vue'

export default {
    name: 'NavItem',

    components: {
        NavLink,
    },

    data() {
        return {
            store,
        }
    },

    methods: {
    },


}
</script>

<template>
    <nav>
        <div class="small-container d-flex justify-content-between align-items-center">
            <div class="btn-container">
                <div class="button oswald-medium text-uppercase">
                    order online
                </div>
            </div>
            <img class="logo" src="/img/h5-logo-divided-header.png" alt="">
            <ul class="links d-flex list-unstyled oswald-medium text-white text-uppercase">
                <NavLink v-for="currentLink in store.link" :link="currentLink"></NavLink>

            </ul>
            <ul class="right d-flex gap-1">
                <div class="icon d-flex align-items-center">
                    <img src="/svg/svg-1.svg" alt="">
                    <a href="#" class="oswald-medium text-white text-uppercase">cart</a>
                </div>

                <div class="icon d-flex align-items-center">
                    <img src="/svg/svg-12.svg" alt="">
                    <a href="#" class="oswald-medium text-white text-uppercase">search</a>
                </div>
            </ul>
        </div>

    </nav>

</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

.small-container {
    position: relative;
    padding: 50px 0;

    .logo {
        position: absolute;
        height: 100px;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }

    .btn-container {
        .button {
            background-color: $primary;
            color: white;
            font-size: 13px;
            letter-spacing: 2px;
            padding: 15px 25px;
        }
    }

    .links {
        gap: 10px;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);



    }

    .right {

        .icon {
            padding: 15px;
            gap: 5px;
            cursor: pointer;

            img {
                height: 20px;
            }

            a {
                text-decoration: none;
                color: white;
                font-size: .8em;
                letter-spacing: 2px;
            }
        }

    }


}
</style>