<template>
  <base-button color="black">Primary Button</base-button>
</template>

<script>
import BaseButton from './components/BaseButton.vue';
export default {
  name: 'App',
  components: {
    BaseButton,
  },
};
</script>

<style lang="scss">
body {
  font-size: 16px;
}
</style>
