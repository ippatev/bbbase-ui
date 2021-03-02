<script>
import { h } from 'vue';
export default {
  render() {
    return h(
      'button',
      {
        class: ['bbb-btn'],
      },
      this.$slots.default()
    );
  },
};
</script>
