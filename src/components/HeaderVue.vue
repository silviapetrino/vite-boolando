
<script>
export default {
 name: "header"
}

</script>

<template>
  

  <header id="topbar">
    <div class="container display-flex">
      <nav>
        <ul>
          <li><a href="">Donna</a></li>
          <li><a href="">Uomo</a></li>
          <li><a href="">Bambini</a></li>
        </ul>
      </nav>
      <div id="logo">
        <img src="../../public/img/boolean-logo.png" alt="logo" title="logo-boolean">
      </div>
      <nav>
        <ul>
          <li>
            <a href="">
              <i class="fa-regular fa-user"></i>
            </a>
          </li>
          <li>
            <a href="">
              <i class="fa-regular fa-heart"></i>
            </a>
          </li>
          <li>
            <a href="">
              <i class="fa-solid fa-bag-shopping"></i>
            </a>
          </li>
        </ul>
      </nav>
    </div>
  </header>


</template>

<style lang="scss" scoped>

@use '../scss/partials/header.scss'

</style>