<template>
  <div>
    <img :src="$router.options.base + 'tako.png'" alt="tako" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage',
})
</script>
