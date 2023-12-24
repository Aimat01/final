<template>
  <div class="icons">
    <img :src="src" :alt="altText" :title="titleText"/>
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
      default: '30px'
    }
  }
};
</script>

<style scoped>
/* Add any custom styles here if needed */
img{
  width: 17px;
  height: 17px;
}
.icons{
  padding-top: 7px;
}
</style>
