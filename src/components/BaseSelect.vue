<template>
  <select class="bbb-select">
    <option v-for="op in options" :key="op.id" :value="op.id"
      >{{ op.value }}
    </option>
  </select>
</template>
<script>
export default {
  props: {
    options: Array,
  },
};
</script>
