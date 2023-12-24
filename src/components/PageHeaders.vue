<template>
    <div class="containerHead">
        <Drawers>
          <h3>Zomur</h3>
          <h5>Menu</h5>
          <div class="header__birge">
            <Icons src="https://cdn-icons-png.flaticon.com/128/1946/1946488.png"></Icons>
            <DropButton title="Dashboards" links="12"></DropButton>
          </div>
          <div class="header__birge">
            <Icons src="https://cdn-icons-png.flaticon.com/128/7327/7327006.png"></Icons>
            <Button title="Transaction"></Button>
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
            <DropButton title="Statistics" links="12"></DropButton>
          </div>
          <div class="header__birge">
            <Icons src="https://cdn-icons-png.flaticon.com/128/3781/3781605.png"></Icons>
            <Button title="Inbox"></Button>
          </div>
          <div class="header__birge">
            <Icons src="https://cdn-icons-png.flaticon.com/128/7268/7268615.png"></Icons>
            <DropButton title="External" links="12"></DropButton>
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
              <Search></Search>
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
  