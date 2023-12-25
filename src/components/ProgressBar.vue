<template>
  <div class="progress-bar-container">
    <div class="progress-bar" :style="{ width: progress + '%' }" :class="progressColor"></div>
  </div>
</template>

<script>
export default {
  props: {
    value: {
      type: Number,
      default: 0,
      validator: value => value >= 0 && value <= 100
    }
  },
  computed: {
    progress() {
      return this.value;
    },
    progressColor() {
      if (this.value >= 70) {
        return 'blue-color';
      } else if (this.value >= 50) {
        return 'yellow-color';
      } else {
        return 'red-color';
      }
    }
  }
};
</script>

<style scoped>
.progress-bar-container {
  width: 100%;
  background-color: #e0e0e0;
  height: 20px;
  border-radius: 10px;
}

.progress-bar {
  height: 100%;
  border-radius: 8px;
  transition: width 0.3s ease-in-out;
}

.blue-color {
  background-color: blue;
}

.yellow-color {
  background-color: yellow;
}

.red-color {
  background-color: red;
}
</style>
