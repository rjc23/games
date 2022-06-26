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

<style>
  html, body {
    margin: 0;
    padding: 0;
  }
  .content {
    margin: 0 150px;
    margin-top: 80px;
  }
</style>
