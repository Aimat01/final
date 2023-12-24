<template>
  <span :style="textStyle">{{ content }}</span>
</template>

<script>
export default {
  props: {
    content: {
      type: String,
      required: true
    },
    fontSize: {
      type: String,
      default: '16px'
    },
    color: {
      type: String,
      default: 'black'
    },
    fontWeight: {
      type: [String, Number],
      default: 'normal' // Default to 'normal' if not provided
    }
  },
  computed: {
    textStyle() {
      return {
        fontSize: this.fontSize,
        color: this.color,
        fontWeight: this.fontWeight
      };
    }
  }
}
</script>

<style scoped>
/* Add any additional styling here if necessary */
</style>
  