<template>
  <body>
    <div class="container">
      <div class="accordion">
        <Collapse v-for="(item, index) in items" class="accordion__body" :item="item" :index="index" />
      </div>
    </div>
  </body>
</template>

<script>
  import Collapse from './Collapse2.vue'

  export default{
    data(){
      return{
        items: [
          {
            question: "They don't know me son",
            answer: "Yes sir!"
          },
          {
            question: "Problems?",
            answer: "No sir!"
          },
          {
            question: "Dosyyyyyyyym",
            answer: "Yep Yep"
          },
          {
            question: "Don Toliver",
            answer: "Mystery Lady"
          }
        ]
      }
    },
    components:{
      Collapse
    }
  }
</script>

<style>
  .accordion{
    display: grid;
  }
  .accordion__body{
    width: 100%;
    max-width: 768px;
    margin: 10px auto;
    padding: 10px;
    border-radius: 8px;
    background-color: white;
    color: black;
  }
</style>
