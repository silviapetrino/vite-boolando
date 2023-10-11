
<script>
import socialicons from '../data/socialicons';

export default {
    name: "footer",

    data() {
      return {
        socialicons
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
          <li><a href="">Informazioni legali</a></li>
          <li><a href="">Informativa di privacy</a></li>
          <li><a href="">Diritto di recesso</a></li>
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