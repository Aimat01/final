<template>
  <div class="card">
    <img :src="src" :alt="altText" class="card-image">
    <div class="card-content">
      <h2 class="card-title">{{ title }}</h2>
      <p class="card-text">{{ content }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    src: {
      type: String,
      required: true,
    },
    altText: {
      type: String,
      default: 'Card Image',
    },
    title: {
      type: String,
      required: true,
    },
    content: {
      type: String,
      default: '',
    },
  },
};
</script>

<style scoped>
.card {
  display: flex;
  align-items: center;
  transition: transform 0.3s ease;
}
.card-image {
  width: 20%;
  height: 40px;
  display: block;
}

.card-title {
  margin-top: 0;
  margin-bottom: 8px;
  font-size: 12px;
  color: #333;
}

.card-text {
  color: #666;
  font-size: 10px;
}
</style>
