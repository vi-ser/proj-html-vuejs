<script>
export default {
    name: 'RestaurantItem',

    props: {
        restaurant: Object,
    }
}
</script>

<template>
    <li>
        <span>{{ restaurant.address }}</span><br>
        <span>{{ restaurant.city }}</span><br>
        <span>{{ restaurant.phone }}</span>
    </li>
</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

li {
    color: $textLight;
    font-size: .8em;
    margin-bottom: 25px;
}
</style>