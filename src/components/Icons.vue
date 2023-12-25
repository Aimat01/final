<template>
  <div class="icons">
    <img :src="src" :alt="altText" :title="titleText" :width="size" :height="size1"/>
  </div>
</template>

<script>
export default {
  props: {
    src: {
      type: String,
      required: true,
      default: ''
    },
    altText: {
      type: String,
      default: 'Icon'
    },
    titleText: {
      type: String,
      default: 'Icon'
    },
    size:{
      type: String,
      default: '17px'
    },
    size1:{
      type: String,
      default: '17px'
    }
  }
};
</script>

<style scoped>
/* Add any custom styles here if needed */
.icons{
  padding-top: 7px;
}
</style>
