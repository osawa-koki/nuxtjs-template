<template>
  <header>
    <nav>
      <ul id="Links">
        <li v-for="page in pages" :key="page.name">
          <nuxt-link :to="page.path">
            {{ page.name }}
          </nuxt-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import pages from '~/pages';

export default defineComponent({
  name: 'HeaderDiv',
  data() {
    return {
      pages,
    }
  },
})
</script>

<style lang="scss" scoped>
#Links {
  display: flex;
  list-style: none;
  li {
    margin-right: 0.5rem;
    margin-bottom: 1rem;
    padding-right: 0.5rem;
    border-right: 1px lightgray solid;
    a {
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
header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  height: 70px;
  background-color: rgba(white, 0.99);
  z-index: 100;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  max-width: 1500px;
  margin: 0 auto;
  nav {
    margin: 0;
    padding: 0;
    position: absolute;
    inset: 0;
    display: flex;
    align-items: center;
    #Links {
      margin: 0;
      padding: 1rem;
      position: absolute;
      inset: 0;
    }
  }
}
</style>

