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


<div class="container display-flex">

    <Card />

</div>
  

</template>

<style lang="scss" scoped>



</style>