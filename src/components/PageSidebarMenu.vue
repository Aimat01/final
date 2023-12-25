<template>
    <div class="sidebar">
      <div class="sidebar-header">
        <div class="sidebar__column1">
          <div class="sidebar__row">
            <div class="sidebar__row__circle">
              <RingPieChart size="100" percentage1="11.5" percentage2="88.5" color2="#9cb6ff" centerText="11.5%"></RingPieChart>
              <div class="sidebar__row__info">
                <div class="sidebar__row__info__name">
                  <Text content="Total Sells"></Text>
                  <div class="sidebar__row__info__img">
                    <UserProfileImg class='image1' shape="circle" size="25px"></UserProfileImg>
                    <UserProfileImg class='image2' shape="circle" size="25px"></UserProfileImg>
                    <UserProfileImg class='image3' shape="circle" size="25px"></UserProfileImg>
                  </div>
                </div>  
                <div class="sidebar__row__info__count">
                  <Text content="40,55K" fontWeight="bold"></Text>
                  <div class="sidebar__row__info__count-h">
                    <Icons src="https://cdn-user-icons.flaticon.com/123098/123098580/1703434485075.svg?token=exp=1703435385~hmac=e71f241d2f2ce665f4780edb4364697d" size="12px" size1="12px"></Icons>
                    <h5>59%</h5>
                  </div>
                </div>
              </div>
            </div>
            <div class="sidebar__row__circle">
              <RingPieChart size="100" percentage1="75.5" percentage2="24.5" color2="#9cb6ff" centerText="75.5%"></RingPieChart>
              <div class="sidebar__row__info">
                <div class="sidebar__row__info__name">
                  <Text content="Views Our Adds"></Text>
                  <div class="sidebar__row__info__img">
                    <UserProfileImg class='image4' shape="circle" size="25px"></UserProfileImg>
                    <UserProfileImg class='image5' shape="circle" size="25px"></UserProfileImg>
                    <UserProfileImg class='image6' shape="circle" size="25px"></UserProfileImg>
                  </div>
                </div>
                <div class="sidebar__row__info__count">
                  <Text content="40,55K" fontWeight="bold"></Text>
                  <div class="sidebar__row__info__count-h">
                    <Icons src="https://cdn-user-icons.flaticon.com/123098/123098580/1703434485075.svg?token=exp=1703435385~hmac=e71f241d2f2ce665f4780edb4364697d" size="12px" size1="12px"></Icons>
                    <h5>75%</h5>
                  </div>
                </div>
              </div>
            </div>
            <div class="sidebar__row__circle">
              <RingPieChart size="100" percentage1="52.5" percentage2="47.5" color2="#9cb6ff" centerText="52.5%"></RingPieChart>
              <div class="sidebar__row__info">
                <div class="sidebar__row__info__name">
                  <Text content="Total Click"></Text>
                  <div class="sidebar__row__info__img">
                    <UserProfileImg class='image7' shape="circle" size="25px"></UserProfileImg>
                    <UserProfileImg class='image8' shape="circle" size="25px"></UserProfileImg>
                    <UserProfileImg class='image9' shape="circle" size="25px"></UserProfileImg>
                  </div>
                </div>
                <div class="sidebar__row__info__count">
                  <Text content="40,55K" fontWeight="bold"></Text>
                  <div class="sidebar__row__info__count-h">
                    <Icons src="https://cdn-user-icons.flaticon.com/123098/123098580/1703434485075.svg?token=exp=1703435385~hmac=e71f241d2f2ce665f4780edb4364697d" size="12px" size1="12px"></Icons>
                    <h5>35%</h5>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="sidebar__row1">
            <div class="sidebar__rov1-name">
              <h4>Sell History</h4>
              <div class="sidebar__rov1-info">
                <Icons src="https://cdn-user-icons.flaticon.com/123098/123098580/1703439633429.svg?token=exp=1703440534~hmac=98168563929e24772fe63de9cfe9a201"></Icons>
                <h5>Avg: Sell Price</h5>
                <Icons src="https://cdn-user-icons.flaticon.com/123098/123098580/1703439656399.svg?token=exp=1703440556~hmac=94a75d9841b3a41b09df2afe76aca41c"></Icons>
                <h5>Avg: Sell Price</h5>
              </div>
              <DropButton :options="dropdownOptions" @selected="handleSelected" initialText="Last 7 days"></DropButton>
            </div>
            <div class="sidebar__rov1-barchart">
              <div class="sidebar__rov1-barchart-percent">
                <h4>100%</h4>
                <h4>80%</h4>
                <h4>60%</h4>
                <h4>40%</h4>
                <h4>20%</h4>
                <h4>0%</h4>
              </div>
              <div class="sidebar__rov1-barchart-graph">
                <BarChart class="elem" v-for="(element, index) in styles"  
                          :key="index"  
                          :title="element.elementName"  
                          :color1="element.color1" 
                          :color2="element.color2" 
                          :height1="element.height1" 
                          :height2="element.height2" 
                          > 
                </BarChart>
              </div>
              <div class="sidebar__rov1-piechart">
                <Text content="Sale Report" fontWeight="700"></Text>
                <PieChart/>
              </div>
            </div>
          </div>
          <div class="sidebar__row3">
            <div class="sidebar__row-search">
              <Icons src="https://cdn-icons-png.flaticon.com/128/622/622669.png"></Icons>
              <div class="sidebar__row-search-input">
                <Search></Search>
              </div>
            </div>
            <div class="sidebar__row-app">
              <div class="sidebar__row-app1">
                <Icons src="https://cdn-icons-png.flaticon.com/128/3024/3024539.png"></Icons>
                <Text content="Filters"></Text>  
              </div>
              <div class="sidebar__row-app1">
                <Icons src="https://cdn-icons-png.flaticon.com/128/747/747310.png"></Icons>
                <DateTime></DateTime>
              </div>
              <div class="sidebar__row-app1">
                <Icons src="https://cdn-icons-png.flaticon.com/128/2258/2258853.png"></Icons>
                <Text content="Download"></Text>  
              </div>
            </div>
          </div>
          <div class="sidebar__row">
            <Table :headers="headers" :rows="rows"></Table>
          </div>
          <div class="sidebar__row4">
            <Pagination :totalItems="totalItems" :itemsPerPage="10"></Pagination>
          </div>
        </div>
        <div class="sidebar__column2">
          <div class="sidebar__column-big">
            <Text content="My Wallet" fontWeight="700"></Text>
            <Bar height="150px" width="300px"></Bar>
          </div>
          <div class="sidebar__column-big2">
            <Text content="Sales History" fontWeight="700"></Text>
            <div class="sidebar__column-card">
              <UserProfileImg></UserProfileImg>
              <div class="sidebar__column-card-info">
                <Text content="Aimat Kulmakhan" fontWeight="700"></Text>
                <div class="sidebar__column-card-cost">
                  <Text content="$400.98" color="#0076fc"></Text>
                  <Text content="April 29 2022"></Text>
                </div>
              </div>
              <Text content="+324.75%" color="#2bd60d"></Text>
            </div>
            <div class="sidebar__column-card">
              <UserProfileImg></UserProfileImg>
              <div class="sidebar__column-card-info">
                <Text content="Aimat Kulmakhan"></Text>
                <div class="sidebar__column-card-cost">
                  <Text content="$550.75" color="#0076fc"></Text>
                  <Text content="April 28 2022"></Text>
                </div>
              </div>
              <Text content="-324.75%" color="#d60d32"></Text>
            </div>
            <div class="sidebar__column-card">
              <UserProfileImg></UserProfileImg>
              <div class="sidebar__column-card-info">
                <Text content="Aimat Kulmakhan"></Text>
                <div class="sidebar__column-card-cost">
                  <Text content="$210.98" color="#0076fc"></Text>
                  <Text content="April 29 2022"></Text>
                </div>
              </div>
              <Text content="+324.75%" color="#2bd60d"></Text>
            </div>
          </div>
          <div class="sidebar__column-big">
            <Text content="Select Date" fontWeight="700"></Text>
            <Calendar></Calendar>
          </div>
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
import Icons from './Icons.vue';
import BarChart from './BarChart.vue';
import DropButton from './DropButton.vue';
import Search from './Search.vue';
import DateTime from './DateTime.vue';
import DatePicker from './DatePicker.vue';
import Card from './Card.vue';
import Image from './Image.vue';
import Calendar from './Calendar.vue'
import PieChart from './PieChart.vue'
import Pagination from './Pagination.vue';

import Aimat from './assets/WIN_20231222_04_47_32_Pro.jpg'
import RingPieChart from './RingPieChart.vue';

  export default {
    name: 'Sidebar',
    components: {
    Circle,
    Text,
    UserProfileImg,
    Bar,
    Table,
    Icons,
    BarChart,
    DropButton,
    Search,
    DateTime,
    DatePicker,
    Card,
    Image,
    Calendar,
    PieChart,
    RingPieChart,
    Pagination
},
    data(){
      return{
        Aimat,
        headers:['','Customer name', 'Date', 'Amount', 'Payment', 'Status'],
        rows:[
          ['','Jenny Wilson', 'Apr 27, 2023', '$3,987.00', 'Paid', 'Unfulfilled'],
          ['','Eleanor Pena', 'Apr 24, 2023', '$7,987.00', 'Unpaid', 'Cancelled'],
          ['','Guy Hawkins', 'Apr 27, 2023', '$3,987.00', 'Paid', 'Unfulfilled'],
          ['','Kristin Watson', 'Apr 27, 2023', '$3,987.00', 'Paid', 'Unfulfilled'],
          ['','Wade Warren', 'Apr 24, 2023', '$7,987.00', 'Unpaid', 'Cancelled'],
          ['','Kristin Watson', 'Apr 27, 2023', '$3,987.00', 'Paid', 'Unfulfilled']
        ],
        styles: [ 
                    {elementName: 'Jan', color1: '#cde5ff', height1: '60%' , color2:'#cde5ff' , height2: '50%'}, 
                    {elementName: 'Feb', color1: '#cde5ff', height1: '70%' , color2:'#cde5ff' , height2: '60%'}, 
                    {elementName: 'Mar', color1: '#cde5ff', height1: '30%' , color2:'#cde5ff' , height2: '20%'}, 
                    {elementName: 'Apr', color1: '#007bff', height1: '72%' , color2:'rgba(241,199,103,255)' , height2: '80%'}, 
                    {elementName: 'May', color1: '#cde5ff', height1: '55%' , color2:'#cde5ff' , height2: '60%'}, 
                    {elementName: 'Jun', color1: '#cde5ff', height1: '70%' , color2:'#cde5ff' , height2: '60%'}, 
                    {elementName: 'Jul', color1: '#cde5ff', height1: '85%' , color2:'#cde5ff' , height2: '80%'}, 
                    {elementName: 'Aug', color1: '#cde5ff', height1: '40%' , color2:'#cde5ff' , height2: '43%'}, 
                    {elementName: 'Sep', color1: '#cde5ff', height1: '42%' , color2:'#cde5ff' , height2: '37%'}, 
                    {elementName: 'Oct', color1: '#cde5ff', height1: '25%' , color2:'#cde5ff' , height2: '27%'}, 
                    {elementName: 'Nov', color1: '#cde5ff', height1: '70%' , color2:'#cde5ff' , height2: '72%'}, 
                    {elementName: 'Dec', color1: '#cde5ff', height1: '61%' , color2:'#cde5ff' , height2: '70%'}, 
                ] ,
        dropdownOptions: ['Last 30 days', 'Last 60 days', 'Last 90 days'],
        totalItems: 100, // For example, total number of items in your list
        currentPageItems: [6], // Your list of items for the current page
        // ... any other data properties you might have
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
    gap:100px;
  }  
  .sidebar__row1{
    padding-top: 50px;
    padding-left: 10px;
    display: block;
  }
  .sidebar__row3{
    padding-top: 40px;
    display: flex;
    justify-content: space-around;
  } 
  .sidebar__row4{
    display: flex;
    justify-content: center;
    padding-top: 20px;
    padding-left: 90vh;
  } 
  .sidebar__rov1-piechart{
    margin-top: -30px;
    padding-left: 60px;
    display: grid;
  }
  .sidebar__column-card{
    display: flex;
    gap: 15px;
    align-items: center;
  }
  .sidebar__rov1-info{
    display: flex;
    gap: 6px;
    align-items: center;
  }
  .sidebar__row-search{
    display: flex;
    align-items: center;
  }
  .sidebar__column-big2{
    padding-top: 20px;
    padding-bottom: 20px;
  }
  .sidebar__row-search-input{
    padding-top: 35px;
  }
  .sidebar__row-app{
    display: flex;
    gap:30px;
  }
  .sidebar__row-app1{
    display: flex;
    gap:7px;
    align-items: center;
  }
  .sidebar__rov1-name{
    display: flex;
    gap: 115px;
  }
  .sidebar__rov1-name h4, h5{
    font-weight: 700;
  }
  .sidebar__rov1-barchart{
    display: flex;
    gap: 10px;
  }
  .sidebar__rov1-barchart-percent{
    line-height: 35px;
  }
  .sidebar__rov1-barchart-percent h4{
    font-weight: 400;
  }
  .sidebar__rov1-barchart-graph{
    display: flex;
  }
  .sidebar__row__circle{
    display: flex;
  }
  .sidebar__column-card-cost{
    display: flex;
    gap:15px;
    padding-right: 20px;
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

  .sidebar__row__info__count-h{
    display: flex;
    background-color: #cde5ff;
    align-items: center;
    border-radius: 10px;
    padding: 1px 7px;
  }

  .sidebar__row__info__count h5{
    padding-left: 3px;
    color: #007bff;
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
  .image {
    position: absolute; /* Position images relative to the container */
    width: 100%; /* Adjust as needed */
    height: 100%; /* Adjust as needed */
  }
/* 
  .image1 {
    z-index: 1; 
    right: 34%;
    top: 23%;
  }

  .image2 {
    z-index: 2;
    right: 33%; 
    top: 23%; 
  }

  .image3 {
    z-index: 3;
    right: 32%;
    top: 23%;
  } */

  .image4 {
    z-index: 1; /* This will be on top */
    right: 6%;
    top: 23%;
  }

  .image5 {
    z-index: 2; /* This will be in the middle */
    right: 5%; /* Adjust to cover a bit of the first image */
    top: 23%; /* Adjust to cover a bit of the first image */
  }

  .image6 {
    z-index: 3; /* This will be at the bottom */
    right: 4%; /* Adjust as needed */
    top: 23%; /* Adjust as needed */
  }

  .image7 {
    z-index: 1; /* This will be on top */
    left: 16%;
    top: 23%;
  }

  .image8 {
    z-index: 2; /* This will be in the middle */
    left: 17%; /* Adjust to cover a bit of the first image */
    top: 23%; /* Adjust to cover a bit of the first image */
  }

  .image9 {
    z-index: 3; /* This will be at the bottom */
    left: 18%; /* Adjust as needed */
    top: 23%; /* Adjust as needed */
  }
  </style>