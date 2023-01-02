<template>
  <div>
    <HeaderDiv />
    <main>
      <h2>Nuxt.jsについて思ったこと。</h2>
      <p>Nuxt.jsに関する個人的に思った特徴の説明。</p>
      <hr>
      <p>HTML&amp;CSS&amp;JSをひとつのファイルでコンポーネントとして管理するため、機能ではなく部品としての管理がされています。</p>
      <p>双方向バインディングであるため、比較的簡単に実現したい機能を実現できる一方で、大規模なシステムでは処理が複雑化しそうです。</p>
      <p>ディレクトリ構成が定められているため、保守性は高い一方で複雑なシステムへの対応は困難に思えます。<br />僕的にはディレクトリ構成が公式で定められている方が好きです。</p>
      <p>TypeScriptへの対応が弱い?<br />enum型など、完全にTypeScript独自のデータをテンプレートの中で使うことができなさそうです。<br />もっとも、enum型を避けるように書いている記事も多いので、これはNuxtに限定されたものではありませんが、、、</p>
      <p>React(Next.js)と比べると直感的に書くことができます。<br />VueファイルはあくまでもHTML・CSS・JSです、React(Next.js)のようなJSX(TSX)などとは異なりますので、取得はしやすそうです。<br />個人的にはDOMをよりJSオブジェクトっぽくReact(Next.js)のほうが好みですが、、、</p>
      <p></p>
    </main>
    <FooterDiv />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import pages from '~/pages';

export default defineComponent({
  name: 'IndexPage',
  data() {
    return {
      pages,
    }
  },
})
</script>

<style lang="scss" scoped>
.Central {
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 100vh;
  h1 {
    margin-top: 1rem;
  }
  img {
    margin-top: 1rem;
    border-radius: 50%;
    border: 1px lightgray solid;
  }
}
#Contents {
  display: flex;
  list-style: none;
  padding: 0;
  li {
    margin-right: 0.5rem;
    margin-bottom: 1rem;
    padding-right: 0.5rem;
    border-right: 1px lightgray solid;
    &:last-child {
      margin-right: 0;
      padding-right: 0;
      border-right: none;
    }
    a {
      font-size: 1.1rem;
      color: #0E6DFE;
      text-decoration: none;
      &:hover {
        text-decoration: underline;
      }
    }
  }
}
</style>
