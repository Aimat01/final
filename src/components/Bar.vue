<template>
  <div :style="barStyle" class="bar">
    <div class="text">
      <div class="text__name">
        <Text content="Zomur" color="white"></Text>
      </div>
      <div class="text__info">
        <div class="text__info-balance">
          <Text content="My Balance" color="lightgray" fontSize="13.5px"></Text>
          <Text content="$25,463.00" color="white" fontSize="19px" fontWeight="bold"></Text>
        </div>
        <div class="text__info-percent">
          <Icons src="https://cdn-user-icons.flaticon.com/123098/123098580/1703434379375.svg?token=exp=1703435287~hmac=bb5cf56f99cddd2fd6c2f9409cb52171" size="12px" size1="12px"></Icons>
          <Text content="+2.5%" color="white"></Text>
        </div>
      </div>
      <div class="text__button">
        <Button title="Deposit" background-color="#ffb71c" padding="10px 15px"></Button>
        <Button title="Withdraw" background-color="#ebebeb" padding="10px 15px"></Button>
      </div>
    </div>
  </div>
</template>

<script>
import Text from './Text.vue';
import Button from './Button.vue'
import Icons from './Icons.vue';

export default {
  props: {
    width: {
      type: String,
      required: true
    },
    height: {
      type: String,
      required: true
    },
    color: {
      type: String,
      default: 'blue'
    }
  },
  computed: {
    barStyle() {
      return {
        width: this.width,
        height: this.height,
        backgroundColor: this.color,
        display: 'inline-block'
      };
    }
  },
  components:{
    Text,
    Button,
    Icons
  }
}
</script>

<style scoped>
/* Add any additional styling here if needed */
.bar{
  border-radius: 10px;
}

.text{
  padding-left: 25px;
}
.text__info{
  display: flex;
  /* justify-content: space-between; */
  gap:110px
}
.text__info-balance{
  display: grid;
}
.text__info-percent{
  display: flex;
  align-items: center;
}
.text__button{
  display: flex;
  padding-left: 25px;
  gap:15px
}
</style>
