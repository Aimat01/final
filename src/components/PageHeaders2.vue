<template>
    <div class="containerHead">
        <Drawers>
          <h3>Zomur</h3>
          <h5>Menu</h5>
          <div class="header__birge">
            <Icons src="https://cdn-icons-png.flaticon.com/128/1946/1946488.png"></Icons>
            <a href="../../index.html"><DropButton :options="dropdownOptions" @selected="handleSelected" initialText="Dashboard"></DropButton></a>
          </div>
          <div class="header__birge">
            <Icons src="https://cdn-icons-png.flaticon.com/128/7327/7327006.png"></Icons>
            <a href="../../index3.html"><Button title="Transaction"></Button></a>
          </div>
          <div class="header__birge">
            <Icons src="https://cdn-icons-png.flaticon.com/128/2169/2169864.png"></Icons>
            <Button title="My Wallet"></Button>
          </div>
          <div class="header__birge">
            <Icons src="https://cdn-icons-png.flaticon.com/128/993/993762.png"></Icons>
            <Button title="Analytics"></Button>
          </div>
          <div class="header__birge">
            <Icons src="https://cdn-icons-png.flaticon.com/128/2936/2936690.png"></Icons>
            <DropButton :options="dropdownOptions" @selected="handleSelected" initialText="Statistics"></DropButton>
          </div>
          <div class="header__birge">
            <Icons src="https://cdn-icons-png.flaticon.com/128/3781/3781605.png"></Icons>
            <Button title="Inbox"></Button>
          </div>
          <div class="header__birge">
            <Icons src="https://cdn-user-icons.flaticon.com/123098/123098580/1703462841044.svg?token=exp=1703463741~hmac=e4359ae34d93d51d63bf747dad4677a5"></Icons>
            <a href="../../index2.html"><DropButton :options="dropdownOptions" @selected="handleSelected" initialText="External" initialColor="#007bff"></DropButton></a>
          </div>
          <div class="header__birge">
            <Icons src="https://cdn-icons-png.flaticon.com/128/5956/5956597.png"></Icons>
            <Button title="Project"></Button>
          </div>
          <div class="header__birge">
            <Icons src="https://cdn-icons-png.flaticon.com/128/9915/9915913.png"></Icons>
            <Button title="Integrations"></Button>
          </div>
          <div class="header__birge">
            <Icons src="https://cdn-icons-png.flaticon.com/128/1827/1827392.png"></Icons>
            <Button title="Notifications"></Button>
          </div>
          <div class="header__birge">
            <Icons src="https://cdn-icons-png.flaticon.com/128/1946/1946429.png"></Icons>
            <Button title="User"></Button>
          </div>
          <div class="header__birge">
            <Icons src="https://cdn-icons-png.flaticon.com/128/3503/3503786.png"></Icons>
            <Button title="History"></Button>
          </div>
          <h5>Help</h5>
          <div class="header__birge">
            <Icons src="https://cdn-icons-png.flaticon.com/128/1067/1067566.png"></Icons>
            <Button title="Support"></Button>
          </div>
          <div class="header__birge">
            <Icons src="https://cdn-icons-png.flaticon.com/128/2040/2040504.png"></Icons>
            <Button title="Setting"></Button>
          </div>
          <div class="header__birge">
            <Icons src="https://cdn-icons-png.flaticon.com/128/1828/1828427.png"></Icons>
            <Button title="Logout"></Button>
          </div>
        </Drawers>
        <div class="page-header">
            <div class="page-header-name">
              <h1>{{ title }}</h1>
              <p v-if="description">{{ description }}</p>
            </div>
            <div class="page-header-search">
              <Icons src="https://cdn-icons-png.flaticon.com/128/622/622669.png"></Icons>
              <Search></Search>
              <Icons src="https://cdn-icons-png.flaticon.com/128/3024/3024539.png"></Icons>
            </div>
            <div class="page-header-icons">
              <Icons src="https://cdn-icons-png.flaticon.com/128/5373/5373324.png"></Icons>
              <Icons src="https://cdn-icons-png.flaticon.com/128/953/953810.png"></Icons>
              <Icons src="https://cdn-icons-png.flaticon.com/128/2645/2645897.png"></Icons>
              <Icons src="https://cdn-icons-png.flaticon.com/128/2099/2099058.png"></Icons>
              <div class="page-header-profileImg">
                <UserProfileImg shape="square"></UserProfileImg>
              </div>
            </div>
        </div>
    </div>
  </template>
  
  <script>
  import Drawers from './Drawers.vue';
  import DropButton from './DropButton.vue';
  import Icons from './Icons.vue';
  import Search from './Search.vue';
  import UserProfileImg from './UserProfileImg.vue';
  import Button from './Button.vue'

  export default {
    data(){
      return{
        dropdownOptions: ['Option 1 ', 'Option 2', 'Option 3']
      }
    },
    props: {
      title: {
        type: String,
        required: true
      },
      description: {
        type: String,
        default: ''
      }
    },
    components:{
    Search,
    UserProfileImg,
    Icons,
    Drawers,
    DropButton,
    Button
}
  }
  </script>
  
  <style>
  .containerHead h3{
    color: black;
    font-weight: 600;
    font-family: sans-serif;
    display: flex;
    justify-content: center;
  }
  .containerHead h5{
    color: gray;
    padding-left: 13px;
  }
  .page-header {
    display: flex;
    justify-content: space-around;
    padding: 20px;
    color: black;
    background-color: #f5f5f5;
    border-bottom: 1px solid #ddd;
  }
  
  .header__birge{
    display: flex;
    padding-left: 15px;
  }

  .page-header h1 {
    margin: 0;
    font-size: 24px;
    font-weight: 500;
  }
  
  .page-header p {
    margin-top: 10px;
    font-size: 16px;
    color: #777;
  }

  .page-header-search{
    display: flex;
  }

  .page-header-icons{
    display: flex;
    gap:20px;
  }
  </style>
  