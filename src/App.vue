
<script>

import HeaderVue from './components/HeaderVue.vue';
import MainVue from './components/MainVue.vue';
import FooterVue from './components/FooterVue.vue';

export default {
  name: "appVue",
  components: {
    HeaderVue,
    MainVue,
    FooterVue
  }

}
</script>

<template>
  <HeaderVue />
  <MainVue />
  <FooterVue />
</template>


<style lang="scss">

@use "./scss/main.scss";

</style>