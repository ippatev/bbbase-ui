<template>
  <base-button @click="clickHandler">First Button</base-button>
  <base-button class="mt-8" @click="clickHandler">Second Button</base-button>
</template>

<script>
import BaseButton from './components/BaseButton.vue';
export default {
  name: 'App',
  components: {
    BaseButton,
  },
  methods: {
    clickHandler(t) {
      alert(`${t.target.textContent} clicked!`);
    },
  },
};
</script>

<style lang="scss">
@import '@/assets/style/style.scss';
</style>
