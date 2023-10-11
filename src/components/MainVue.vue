<script>
import Cards from './partials/Cards.vue';
import cards from '../data/partials/cards';

export default {
    name: "main",
    components: {
        Cards
    },

    data() {
        cards
    }
}

</script>

<template>

<div class="container">

    <div class="container-main display-flex">

      <Cards />


    </div>

</div>

  

</template>

<style lang="scss" >


</style>