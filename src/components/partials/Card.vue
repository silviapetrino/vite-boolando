
<script>
import cardList from '../../data/partials/card';

export default {
  name: "card",
  data(){
    return {
      cardList
    }
  }
}
</script>

<template>

<div class="card" v-for="(item, index) in cardList" :key="`card-${index}`">

  <img class="first" :src="`../../../public/img/${item.primaryImage}`" :alt="item.gender">
  <img class="second" :src="`../../../public/img/${item.secondaryImage}`" :alt="item.gender">

  <span class="heart">&hearts;</span>
  <div class="marks">
    <span class="range-discount"> {{ item.discount }}</span>
    <span class="value">Sostenibilità</span>
  </div>

<div class="product-details">
    <span class="brand">{{ item.marca }}</span>
    <h4 class="product-name">{{ item.modello }}</h4>
    <span class="price">{{ item.lastPrice }}</span>
    <span class="discount">{{ item.fullPrice }}</span>
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
 


  img {
    width: 100%;
    object-fit: cover;
    z-index: 0;
  }

  img.first:hover {
    display: none;
  }

  img.second {
    display: none;
    &:hover {
      display: block;
    }
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