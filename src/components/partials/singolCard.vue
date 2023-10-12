
<script>

  export default {
    name: "singol-card",
    props: {
      singolCard: Object
    }
  
  }
  
</script>

<template>

  <div class="singol-card card">

    <img class="first" :src="`../../../public/img/${singolCard.primaryImage}`" :alt="singolCard.gender">
    <img class="second" :src="`../../../public/img/${singolCard.secondaryImage}`" :alt="singolCard.gender">

  <span class="heart">&hearts;</span>
  <div class="marks">
    <span class="range-discount"> {{ singolCard.discount }}</span>
    <span v-if="singolCard.sostenibilita" class="value">Sostenibilità</span>
  </div>

  <div class="product-details">
      <span class="brand">{{ singolCard.marca }}</span>
      <h4 class="product-name">{{ singolCard.modello }}</h4>
      <span class="price">{{ singolCard.lastPrice }}</span>
      <span class="discount">{{ singolCard.fullPrice }}</span>
  </div>


  </div>
  
</template>

<style lang="scss" scoped>

.card {
  cursor: pointer;
  background-color: white;
  margin: 5px;
  width: calc(100% / 3 - 10px);
  min-width: 250px;
  position: relative;

  &:hover {
    img.first {
      display: none;
    }
    img.second {
      display: block;
    }
  }
 
  img {
    width: 100%;
    object-fit: cover;
    z-index: 0;
  }

  img.second {
    display: none;
  }

  .product-details {
    width: 100%;

    .brand, .product-name {
      display: block;
      font-size: .8rem;
    }
    .price {
      font-size: .7rem;
      font-weight: 600;
      color: red;
    }
    .discount {
      font-size: .7rem;
      text-decoration: line-through;
    }
  }


  .heart, .marks {
    z-index: 1;
  }
  .heart {
    display: inline-block;
    position: absolute;
    right: 0;
    top: 8px;
    background-color: white;
    width: 30px;
    height: 35px;
    text-align: center;
    line-height: 35px;
    font-size: 25px;
    cursor: pointer;
    &:hover {
      color: red;
    }
  }
  .marks {
    position: absolute;
    top: 80%; 
    left: 0;
    .range-discount, .value {
      display: inline-block;
      color: white;
      font-size: .7rem;
      font-weight: 600;
      padding: 4px 6px;
    }
      .range-discount {
        background-color: red;
      }
      .value {
      background-color: green;
      }

    }
    
  }

  
.card:last-child .value {
 left: 0%;
}


</style>