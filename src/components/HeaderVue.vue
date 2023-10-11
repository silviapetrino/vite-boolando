
<script>
import headerMenu from "../data/headerMenu";
import socialIcons from "../data/socialicons";

export default {
 name: "header",

 data(){
  return {
    headerMenu,
    socialIcons
  }
 }
}

</script>

<template>
  

  <header id="topbar">
    <div class="container display-flex">
      <nav>
        <ul>
          <li v-for="(item, index) in headerMenu" :key="`header-${index}`"><a :href="item.href">{{ item.text }}</a></li>
        </ul>
      </nav>
      <div id="logo">
        <img src="../../public/img/boolean-logo.png" alt="logo" title="logo-boolean">
      </div>
      <nav>
        <ul>
          <li v-for="(icon, index) in socialIcons.headerSocial" :key="`socialHeader-${index}`">
            <a :href="icon.href">
              <i :class="icon.class"></i>
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