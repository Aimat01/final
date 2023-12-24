<template>
    <div class="sidebar">
      <div class="sidebar-header">
        <div class="sidebar__column1">
          <div class="sidebar__row">
            <div class="sidebar__row__circle">
              <Circle content="11.5%" color="blue" size="80px"></Circle>
              <div class="sidebar__row__info">
                <div class="sidebar__row__info__name">
                  <Text content="Total Sells"></Text>
                  <div class="sidebar__row__info__img">
                    <UserProfileImg shape="circle" size="25px"></UserProfileImg>
                    <UserProfileImg shape="circle" size="25px"></UserProfileImg>
                    <UserProfileImg shape="circle" size="25px"></UserProfileImg>
                  </div>
                </div>  
                <div class="sidebar__row__info__count">
                  <Text content="40,55K" fontWeight="bold"></Text>
                  <div class="sidebar__row__info__count-h">
                    <h5>59%</h5>
                  </div>
                </div>
              </div>
            </div>
            <div class="sidebar__row__circle">
              <Circle content="75.5%" color="blue" size="80px"></Circle>
              <div class="sidebar__row__info">
                <div class="sidebar__row__info__name">
                  <Text content="Views Our Adds"></Text>
                  <div class="sidebar__row__info__img">
                    <UserProfileImg shape="circle" size="25px"></UserProfileImg>
                    <UserProfileImg shape="circle" size="25px"></UserProfileImg>
                    <UserProfileImg shape="circle" size="25px"></UserProfileImg>
                  </div>
                </div>
                <div class="sidebar__row__info__count">
                  <Text content="40,55K" fontWeight="bold"></Text>
                  <div class="sidebar__row__info__count-h">
                    <h5>75%</h5>
                  </div>
                </div>
              </div>
            </div>
            <div class="sidebar__row__circle">
              <Circle content="52.5%" color="blue" size="80px"></Circle>
              <div class="sidebar__row__info">
                <div class="sidebar__row__info__name">
                  <Text content="Total Click"></Text>
                  <div class="sidebar__row__info__img">
                    <UserProfileImg shape="circle" size="25px"></UserProfileImg>
                    <UserProfileImg shape="circle" size="25px"></UserProfileImg>
                    <UserProfileImg shape="circle" size="25px"></UserProfileImg>
                  </div>
                </div>
                <div class="sidebar__row__info__count">
                  <Text content="40,55K" fontWeight="bold"></Text>
                  <div class="sidebar__row__info__count-h">
                    <h5>35%</h5>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="sidebar__row">
            <!-- <BarChart></BarChart> -->
          </div>
          <div class="sidebar__row">
            <Table :headers="headers" :rows="rows"></Table>
          </div>
        </div>
        <div class="sidebar__column2">
          <Text content="My Wallet"></Text>
          <Bar height="150px" width="300px"></Bar>
        </div>
      </div>
    </div>
  </template>
  
  <script>
import Circle from './Circle.vue';
import Text from './Text.vue';
import UserProfileImg from './UserProfileImg.vue';
import Bar from './Bar.vue';
import Table from './Table.vue';
// import BarChart from './BarChart.vue';

  export default {
    name: 'Sidebar',
    components: {
    Circle,
    Text,
    UserProfileImg,
    Bar,
    // BarChart,
    Table
    },
    data(){
      return{
        headers:['','Customer name', 'Date', 'Amount', 'Payment', 'Status'],
        rows:[
          ['./assets/square.jpg','Jenny Wilson', 'Apr 27, 2023', '$3,987.00', 'Paid', 'Unfulfilled'],
          ['','Eleanor Pena', 'Apr 24, 2023', '$7,987.00', 'Unpaid', 'Cancelled'],
          ['','Guy Hawkins', 'Apr 27, 2023', '$3,987.00', 'Paid', 'Unfulfilled'],
          ['','Kristin Watson', 'Apr 27, 2023', '$3,987.00', 'Paid', 'Unfulfilled'],
          ['','Wade Warren', 'Apr 24, 2023', '$7,987.00', 'Unpaid', 'Cancelled'],
          ['','Kristin Watson', 'Apr 27, 2023', '$3,987.00', 'Paid', 'Unfulfilled']
        ]
      }
    }
};
  </script>
  
  <style scoped>
  .sidebar {
    padding-top: 40px;
  }
  .sidebar__column1{
    padding-left: 30px;
    display: block;
    justify-content: space-between;
    width: 1200px;
  }
  .sidebar__row{
    display: flex;
    gap:140px;
  }  
  .sidebar__row__circle{
    display: flex;
  }
  .sidebar-header {
    padding-bottom: 20px;
    display: flex;
  }
  .sidebar__row__info{
    display: block;
    padding-left: 10px;
  }
  .sidebar__row__info__name{
    display: flex;
    gap: 20px
  }
  .sidebar__row__info__img{
    display: flex;
  }
  .sidebar__row__info__count{
    display: flex;
    padding-top: 20px;
    gap: 20px;
  }
  .sidebar__row__info__count h5{
    padding: 2px 6px;
    color:#005cbe;
    border-radius: 10px;
    background-color:#cde5ff;
  }
  .sidebar__column2{
    line-height: 40px;
  }
  .sidebar-menu router-link {
    color: #fff;
    text-decoration: none;
    padding: 10px;
    margin-bottom: 5px;
    transition: background-color 0.3s;
  }
  
  .sidebar-menu router-link:hover {
    color: #007bff;
  }
  </style>