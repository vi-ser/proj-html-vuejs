<script>
import { store } from '../store';

export default {
    name: 'NavItem',

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
        <div class="small-container d-flex justify-content-between">
            <div class="btn-container">
                <div class="button oswald-medium text-uppercase">
                    order online
                </div>
            </div>
            <ul class="links">

            </ul>
            <ul class="links">

            </ul>
        </div>

    </nav>

</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

.small-container {
    padding: 50px 0;

    .btn-container {
        .button {
            background-color: $primary;
            color: white;
            font-size: 13px;
            letter-spacing: 2px;
            padding: 15px 25px;
        }
    }
}
</style>