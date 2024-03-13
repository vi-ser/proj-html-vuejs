<script>
export default {
    name: 'QuoteItem',

    props: {
        quote: Object,
    }
}
</script>

<template>
    <div class="quote">
        <p class="text-uppercase oswald-medium">{{ quote.quote }}</p>
        <span class="text-uppercase oswald-medium">{{ quote.author }}</span>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

.quote {

    padding: 0 100px;

    p {
        font-size: 1.5em;
        margin-bottom: 15px;
        color: $text;
    }

    span {
        color: $primary;
    }

}
</style>