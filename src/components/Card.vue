<template>
  <div class="container">
    <div class="card">
      <img :src="src" alt="Card Image" class="card-image">
      <div class="card-body">
        Aimat Kulmakhan
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    src: {
      type: String,
      required: true
    }
  }
}
</script>

<style>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-top: 40px;
}

.card {
  border: 1px solid #ccc;
  border-radius: 5px;
  overflow: hidden;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
  display: grid;
  justify-content: center;
}

.card-image {
  width: 100%;
  height: auto;
}

.card-body {
  padding: 10px;
  display: flex;
  justify-content: center;
}

.card img{
  width: 300px;
}
</style>
