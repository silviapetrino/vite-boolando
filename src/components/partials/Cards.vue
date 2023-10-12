<script>
import cardList from '../../data/partials/cards';
import singolCard from './singolCard.vue';



export default {
  name: "card",
  data(){
    return {
      cardList
    }
  },
  components: {
    singolCard
  }
}
</script>

<template>

<singolCard v-for="(item, index) in cardList" :key="`card-${index}`" :singolCard="item" />


  
</template>
  


<style lang="scss" scoped>


</style>