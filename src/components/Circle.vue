<template>
  <div :style="circleStyle">
    <div class="circle__text">
      <Text :content="content" color="black" fontSize="12px"></Text>
    </div>
  </div>
</template>

<script>
import Text from './Text.vue';

export default {
  props: {
    size: {
      type: String,
      default: '50px'
    },
    color: {
      type: String,
      default: 'black'
    },
    content: {
      type: String,
      required: true
    },
    background: {
      type: String,
      default: '#ebebeb'  // Set default background to gray
    },
    fontSize: {
      type: String,
      default: '18px'
    }
  },
  computed: {
    circleStyle() {
      return {
        width: this.size,
        height: this.size,
        borderRadius: '50%',
        background: this.background  // Set background color from props
      };
    }
  },
  components: {
    Text
  }
}
</script>

<style scoped>
.circle__text {
  display: flex;
  justify-content: center;
  text-align: center;
  padding-left: 1px;
}
/* Add any additional styling here if necessary */
</style>
