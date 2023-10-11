<script>
import Card from './partials/Card.vue';
import cards from '../data/partials/card';

export default {
    name: "main",
    components: {
        Card
    },

    data() {
        cards
    }
}

</script>

<template>

<div class="container">

    <div class="container-main display-flex">

      <Card />


    </div>

</div>

  

</template>

<style lang="scss" >


</style>