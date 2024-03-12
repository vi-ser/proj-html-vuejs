<script>
export default {
    name: 'BookItem',
}
</script>

<template>
    <div class="form-container d-flex justify-content-center align-content-center">

        <div class="input-container">
            <input type="text" class="input-field border border-1 border-black" placeholder="1 Person">
            <i class="icon fa-solid fa-user-group"></i>
        </div>
        <div class="preposition d-flex justify-content-center text-center">
            <span class="oswald-medium text-uppercase text-white">FOR</span>
        </div>


        <div class="input-container">
            <input type="text" class="input-field border border-1 border-black" placeholder="20/07/2024">
            <i class="icon fa-regular fa-calendar"></i>
        </div>
        <div class="preposition d-flex justify-content-center text-center">
            <span class="oswald-medium text-uppercase text-white">AT</span>
        </div>


        <div class="input-container">
            <input type="text" class="input-field border border-1 border-black" placeholder="7:00 pm">
            <i class="icon fa-regular fa-clock"></i>
        </div>

        <div class="button text-center oswald-medium text-uppercase">
            book a table
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

.form-container {
    padding: 120px 0;
    background-image: url('/img/h3-background-img-3.jpg');
    background-position: right;
    margin-bottom: $smallMargin;

    .input-container {
        position: relative;
        width: max-content;
    }

    .input-field {
        padding: 15px 25px;
        background-color: white;
        font-size: .8em;
        color: $text;
    }

    .icon {
        position: absolute;
        top: 50%;
        right: 25px;
        transform: translateY(-50%);
        color: $accent;
    }

    .preposition {
        width: 40px;
        align-items: center;

    }


    .button {
        margin-left: 40px;
        background-color: $primary;
        color: white;
        font-size: 13px;
        letter-spacing: 2px;
        padding: 15px 25px;
        width: 192.5px;
    }
}
</style>