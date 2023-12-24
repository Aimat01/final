<template>
  <div :style="circleStyle">
    <div class="circle__text">
      <Text :content="content" color="blue" fontSize="18px"></Text>
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
    }
  },
  computed: {
    circleStyle() {
      return {
        width: this.size,
        height: this.size,
        borderRadius: '50%',
        border: '6px ' + this.color + ' solid'
      };
    }
  },
  components:{
    Text
  }
}
</script>

<style scoped>
.circle__text{
  display: flex;
  justify-content: center;
  padding-top: 18px;
}
/* Add any additional styling here if necessary */
</style>
