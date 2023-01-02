<template>
  <footer>🥺 <a href="https://github.com/osawa-koki" target="_blank">@osawa-koki</a> 🥺</footer>
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
footer {
  height: 70px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: lightgray;
}
</style>

