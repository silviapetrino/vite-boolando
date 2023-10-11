

<script>
export default {
    name: "footer"
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
          <li>
            <a href=""><i class="fa-brands fa-square-twitter"></i>
            </a>
          </li>
          <li>
            <a href=""><i class="fa-brands fa-square-facebook"></i>
            </a>
          </li>
          <li>
            <a href=""><i class="fa-brands fa-square-instagram"></i></a>
          </li>
          <li>
            <a href=""><i class="fa-brands fa-square-pinterest"></i></a>
          </li>
          <li>
            <a href=""><i class="fa-brands fa-square-youtube"></i></a></li>
        </ul>
      </nav>
      </div>
      </div>

  <!-- /footer  -->

  </footer>
</template>

<style lang="scss" scoped>


@use '../scss/partials/footer.scss'

</style>