<script>
export default {
    name: 'PizzaItem',

    props: {
        pizza: Object,
    },

}
</script>

<template>
    <li>
        <img class="pizza-img" :src="pizza.image" :alt="pizza.name">
        <div class="pizza-info">

            <span id="pizza-name" class="text-uppercase d-block oswald-medium"> {{ pizza.name }} </span>
            <span id="pizza-price" class="text-uppercase d-block oswald-medium"> {{ pizza.price }} </span>

        </div>
    </li>

</template>


<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

li {
    padding: 0 30px;

    .pizza-img {
        height: 240px;
        margin-bottom: 25px;
    }

    #pizza-name {
        color: $accent;
        margin-bottom: 5px;
    }

    #pizza-price {
        color: $primary;
    }
}
</style>