
<script>
export default {
  name: "card"
}
</script>

<template>

  


<div class="card">
    <img src="../../../public/img/1.webp" alt="uomo">

    <span class="heart">&hearts;</span>
    <div class="marks">
        <span class="range-discount">-50%</span>
        <span class="value">Sostenibilità</span>
    </div>

    <div class="product-details">
        <span class="brand">Levi's</span>
        <h4 class="product-name">RELAXED FIT TEE UNISEX</h4>
        <span class="price">14,99&euro</span>
        <span class="discount">29,99&euro</span>
    </div>
</div>

  
</template>
  


<style lang="scss" scoped>

.card {
  background-color: white;
  margin: 5px;
  width: calc(100% / 3 - 10px);
  min-width: 250px;
  position: relative;
  cursor: pointer;

  img {
    width: 100%;
    object-fit: cover;
    z-index: 0;
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