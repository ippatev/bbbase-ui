<script>
import { h } from 'vue';
export default {
  props: {
    color: {
      type: String,
      default: 'black',
    },
  },
  render() {
    return h(
      'button',
      {
        style: { backgroundColor: this.color },
        class: ['bbb-btn'],
        onClick: this.$emit('click'),
      },
      this.$slots.default()
    );
  },
};
</script>
<style lang="scss">
.bbb-btn {
  display: block;
  border-radius: 8px;
  padding: 0 24px;
  align-items: center;
  border: none;
  width: 200px;
  line-height: 52px;
  min-width: 200px;
  color: white;
  font-size: inherit;
}
</style>
