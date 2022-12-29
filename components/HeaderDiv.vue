<template>
  <header>
    <nav>
      <NuxtLink v-for="page in pages" :key="page.name" :to="page.path">{{ page.name }}</NuxtLink>
    </nav>
  </header>
</template>

<script lang="ts">
import Vue from 'vue';
import pages from '@/common/pages';

export default Vue.extend({
  name: 'HeaderDiv',
  data() {
    return {
      pages,
    };
  },
});
</script>

<style lang="scss" scoped>
header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  max-width: 1500px;
  height: 70px;
  margin: 0 auto;
  background-color: rgba(white, 0.99);
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  nav {
    position: absolute;
    inset: 0;
    padding: 1rem;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    flex-wrap: wrap;
    a {
      margin: auto 0.5rem;
      padding-right: 0.5rem;
      border-right: 1px lightgray solid;
      color: #0E6DFE;
      text-decoration: none;
      &:last-child {
        margin-right: 0;
        padding-right: 0;
        border-right: none;
      }
      &:hover {
        text-decoration: underline;
      }
    }
  }
}
</style>
