<template>
  <div>
    <HeaderDiv />
    <main>
      <h2>Dummy Contact Form 👍</h2>
      <div class="alert alert-info" role="alert">You clicked {{ click_count }} times.</div>
      <button type="button" class="btn btn-primary" @click="clickMe">Click me {{ emoji }}</button>
      <hr />
      <div class="mb-3">
        <label for="mail" class="form-label">Email address</label>
        <input id="mail" v-model="mail" type="email" class="form-control" placeholder="osawa-koki@example.com" />
      </div>
      <div v-if="MailIsValid" class="alert alert-success" role="alert"> your email is valid 💓</div>
      <div v-if="MailIsValid === false" class="alert alert-danger" role="alert"> your email is invalid 😮‍💨</div>
    </main>
    <FooterDiv />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import pages from '~/pages';

const MailRegex = /^[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+$/;
const emojis = ['🥺', '👼', '😭', '😇', '😢', '😇', '😭', '👼', '🥺'];
const GetEmoji = () => emojis[Math.floor(Math.random() * emojis.length)];
let interval: NodeJS.Timer | null = null;

export default defineComponent({
  name: 'IndexPage',
  data() {
    return {
      pages,
      emoji: GetEmoji(),
      click_count: 0,
      click_me_icon: '🥺' as string,
      mail: 'osawa-koki@example.com',
    };
  },
  computed: {
    MailIsValid(): boolean {
      return MailRegex.test(this.mail);
    }
  },
  mounted(): void {
    interval = setInterval(() => {
      // eslint-disable-next-line no-console
      console.log(GetEmoji());
      this.emoji = GetEmoji();
    }, 1000);
  },
  beforeDestroy() {
    if (interval === null) return;
    clearInterval(interval);
  },
  methods: {
    clickMe() {
      this.click_count++;
      if (this.click_count % 3 === 0) {
        this.click_me_icon = '🥺';
      } else {
        this.click_me_icon = '😭';
      }
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
