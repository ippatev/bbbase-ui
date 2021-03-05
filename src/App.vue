<template>
  <div class="container">
    <base-button @click="clickHandler">Button</base-button>
    <base-text-field placeholder="Text Field" class="ml-16"></base-text-field>
    <base-select @input="selectHandler" :options="selects" class="ml-16" />
    <base-checkbox class="ml-16">Checkbox</base-checkbox>
    <base-radio class="ml-16">Radio</base-radio>
  </div>
</template>

<script>
import BaseButton from './components/BaseButton.vue';
import BaseSelect from './components/BaseSelect.vue';
import BaseCheckbox from './components/BaseCheckbox.vue';
import BaseRadio from './components/BaseRadio.vue';
import BaseTextField from './components/BaseTextField.vue';
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
    BaseTextField,
  },
  methods: {
    clickHandler(t) {
      console.log(`${t.target.textContent} clicked!`);
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
