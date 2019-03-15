<template>
  <div>
    <div class="row">
      <app-header></app-header>
    </div>
    <div class="row">
      <search-input></search-input>
    </div>
    <app-footer></app-footer>
  </div>
</template>

<script>

import Header from './Shared/Header.vue'
import Footer from './Shared/Footer.vue'
import SearchInput from './Server/SearchInput.vue'

export default {
  name: 'Home',
  components: {
    appHeader: Header,
    appFooter: Footer,
    SearchInput: SearchInput
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
