<script>
export default {
    name: 'JumboQuotes',

}
</script>
<template>
    <div id="jumbo-quotes" class="d-flex flex-column text-center">
        <img class="quote" src="/svg/quotes.svg">
        <p class="text-uppercase oswald-medium">“forget the trendy pizza shops, this hidden spot makes the best
            new<br>york-style pizza slice in naples”</p>
        <span class="text-uppercase oswald-medium">washington post 2018</span>
        <div class="control">
            <i class="fa-solid fa-circle active"></i>
            <i class="fa-solid fa-circle"></i>
            <i class="fa-solid fa-circle"></i>
        </div>
    </div>

</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

#jumbo-quotes {
    background-image: url('/img/h3-testimonials-bckgrnd.jpg');
    margin-bottom: $smallMargin;
    width: 100%;
    padding: 105px 0 120px;

    .quote {
        height: 55px;
        margin-bottom: 55px;
    }

    p {
        font-size: 1.5em;
        margin-bottom: 15px;
        color: $text;
    }

    span {
        color: $primary;
    }

    .control {
        margin-top: 30px;

        display: flex;
        justify-content: center;
        gap: 5px;

        i {
            font-size: .5em;
            color: $accentLight;

            &.active {
                color: $accent;
            }
        }

    }
}
</style>