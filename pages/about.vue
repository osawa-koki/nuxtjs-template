<template>
  <div>
    <HeaderDiv />
    <main>
      <h1>Hello {{ name }} 💓💓💓</h1>
      <input type="text" class="form-control" @input="Input" />
    </main>
    <FooterDiv />
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import pages from '@/common/pages';

export default Vue.extend({
  name: 'IndexPage',
  data() {
    return {
      pages,
      name: 'Nuxt.js',
    };
  },
  methods: {
    Input(e: any) {
      this.name = e.target.value;
    },
  },
});
</script>

<style lang="scss" scoped>
#MainTopic {
  display: flex;
  flex-direction: column;
  align-items: center;
  h1 {
    margin-top: 1rem;
    font-size: 2rem;
  }
  img {
    margin-top: 1rem;
    width: 100px;
    border-radius: 50%;
    border: 1px lightgray solid;
  }
}
#Links {
  display: flex;
  justify-content: center;
  margin-top: 1rem;
  a {
    font-size: 1.2rem;
    margin-right: 0.5rem;
    margin-bottom: 1rem;
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
</style>
