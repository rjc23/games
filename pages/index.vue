<template>
<div>
  <Header/>
  <div class="content">
    <Games/>
  </div>
</div>
</template>

<script lang="ts">
  import Vue from 'vue'

  export default Vue.extend({
    name: 'IndexPage'
  })
</script>

<style lang="scss">
  @import './../assets/scss/responsive.scss';

  html, body {
    margin: 0;
    padding: 0;
  }
  .content {

    margin-top: 40px;
    @include respond-to(mobile) {
      margin-left: 20px;
      margin-right: 20px;
      margin-top: 80px;
    }
  }
</style>
