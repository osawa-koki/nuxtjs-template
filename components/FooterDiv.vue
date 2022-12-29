<template>
  <footer>nuxtjs-template @osawa-koki</footer>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'FooterDiv',
});
</script>

<style lang="scss" scoped>
footer {
  margin-top: 3rem;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: lightgray;
  width: 100%;
  height: 5rem;
}
</style>
