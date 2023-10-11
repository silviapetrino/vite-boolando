
<script>
import socialicons from '../data/socialicons';
import footerMenu from '../data/footerMenu';

export default {
    name: "footer",

    data() {
      return {
        socialicons,
        footerMenu
      }
    }
}

</script>

<template>
     <footer>
    <div class="container display-flex">
      <div class="text">
        <h5><a href="">Booleando s.r.l</a></h5>
        <nav>
          <ul>
          <li v-for="(item, index) in footerMenu" :key="`footMenu${index}`"><a :href="item.href">{{ item.title }}</a></li>
        </ul>
      </nav>
      </div>
      <div class="social">
        <span>Trovaci anche su</span>
        <nav>
          <ul>
          <li v-for="(icon, index) in socialicons.footerSocial" :key="`footerIcon${index}`">
            <a :href="icon.href"><i :class="icon.class"></i>
            </a>
          </li>
         
        </ul>
      </nav>
      </div>
      </div>

  <!-- /footer  -->

  </footer>
</template>

<style lang="scss" >


@use '../scss/partials/footer.scss'

</style>