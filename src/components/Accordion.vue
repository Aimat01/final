<template>
  <body>
    <div class="container">
      <div class="accordion">
        <Accordion v-for="(item, index) in items" class="accordion__body" :item="item" :index="index" />
      </div>
    </div>
  </body>
</template>

<script>
  import Accordion from './Accordion2.vue'

  export default{
    data(){
      return{
        items: [
          {
            question: "Who is The Best Football player in The World?",
            answer: "Cristiano Ronaldo and Lionel Messi"
          },
          {
            question: "Cheating is the best team",
            answer: "100% information"
          },
          {
            question: "Do you love listening phonk music?",
            answer: "METAMORPHOSIS, LOST ORION, KEROSENE"
          },
          {
            question: "You need to hire some companies",
            answer: "Like Google, Facebook, Apple"
          }
        ]
      }
    },
    components:{
      Accordion
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
