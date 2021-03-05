<template>
  <div class="container">
    <base-button @click="clickHandler">First Button</base-button>
    <base-select @input="selectHandler" :options="selects" class="ml-16" />
    <base-checkbox class="ml-16" />
    <base-radio class="ml-16" />
  </div>
</template>

<script>
import BaseButton from './components/BaseButton.vue';
import BaseSelect from './components/BaseSelect.vue';
import BaseCheckbox from './components/BaseCheckbox.vue';
import BaseRadio from './components/BaseRadio.vue';
export default {
  name: 'App',
  data() {
    return {
      selects: [
        { id: 0, value: 'Dropdown Item' },
        { id: 1, value: 'Dropdown Item' },
      ],
    };
  },
  components: {
    BaseButton,
    BaseSelect,
    BaseCheckbox,
    BaseRadio,
  },
  methods: {
    clickHandler(t) {
      alert(`${t.target.textContent} clicked!`);
    },
    selectHandler(t) {
      console.log(`${t.target.value} selected!`);
    },
  },
};
</script>

<style lang="scss">
@import '@/assets/style/style.scss';
</style>
