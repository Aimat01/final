<template>
    <div class="sidebar">
      <div class="sidebar-header">
        <div class="sidebar__column1">
          <div class="sidebar__row">
            <div class="sidebar__first">
                <div class="sidebar__icons">    
                    <Icons src="https://cdn-icons-png.flaticon.com/128/1828/1828765.png"></Icons>
                    <Icons src="https://cdn-icons-png.flaticon.com/128/9144/9144015.png"></Icons>
                </div>
                <div class="sidebar__show">
                    <Text content="Show:" color="gray"></Text>
                    <Select :options="dropdownOptions" v-model="selectedItem" text="All products"></Select>
                </div>
            </div>
            <div class="sidebar__sort">
                <div class="sidebar__sorting">
                    <Text content="Sort by:" color="gray"></Text>
                    <Select :options="dropdownOptions" v-model="selectedItem" text="Default"></Select>
                </div>
                <div class="sidebar__button">
                    <Button title="Add products" backgroundColor="blue" color="white" padding="10px 15px"></Button>
                </div>
            </div>
          </div>
          <div class="sidebar__row2">
            <div class="sidebar__row-search">
                <Icons src="https://cdn-icons-png.flaticon.com/128/3031/3031293.png"></Icons>
                <div class="sidebar__row-search-input">
                    <Search></Search>
                </div>
            </div>
            <div class="sidebar__row-filter">
                <Icons src="https://cdn-icons-png.flaticon.com/128/3839/3839020.png"></Icons>
                <Text content="Filters"></Text>
            </div>
          </div>
          <div class="sidebar__row3">
            <div class="sidebar__withIcon">
                <Text content="Product info"></Text>
                <Icons src="https://cdn-icons-png.flaticon.com/128/5436/5436326.png"></Icons>
            </div>
            <div class="sidebar__columns">
                <div class="sidebar__withIcon">
                    <Text content="Price"></Text>
                    <Icons src="https://cdn-icons-png.flaticon.com/128/5436/5436326.png"></Icons>
                </div>
                <div class="sidebar__withIcon">
                    <Text content="Stock"></Text>
                    <Icons src="https://cdn-icons-png.flaticon.com/128/5436/5436326.png"></Icons>
                </div>
                <Text content="Statistics"></Text>
            </div>
            <Text content="Active"></Text>
          </div>
          <div class="sidebar__row4">
            <div class="sidebar__info">
                <div class="sidebar__info-user">
                    <UserProfileImg></UserProfileImg>
                    <div class="sidebar__info-name">
                        <Text content="Berkancing"></Text>
                        <Text content="ID: 098134NN"></Text>
                    </div>
                </div>
                    <Text content="$400.98"></Text>
                    <Text content="234"></Text>
                    <div class="sidebar__info-progress">
                        <Text content="Perfect 1.2k sales"></Text>
                        <ProgressBar value="90"></ProgressBar>
                    </div>
                <Toggles></Toggles>
            </div>
            <div class="sidebar__info">
                <div class="sidebar__info-user">
                    <UserProfileImg></UserProfileImg>
                    <div class="sidebar__info-name">
                        <Text content="Berkancing"></Text>
                        <Text content="ID: 098134NN"></Text>
                    </div>
                </div>
                    <Text content="$500.98"></Text>
                    <Text content="340"></Text>
                    <div class="sidebar__info-progress">
                        <Text content="Perfect 960 sales"></Text>
                        <ProgressBar value="70"></ProgressBar>
                    </div>
                <Toggles></Toggles>
            </div>
            <div class="sidebar__info">
                <div class="sidebar__info-user">
                    <UserProfileImg></UserProfileImg>
                    <div class="sidebar__info-name">
                        <Text content="Berkancing"></Text>
                        <Text content="ID: 098134NN"></Text>
                    </div>
                </div>
                    <Text content="$100.98"></Text>
                    <Text content="744"></Text>
                    <div class="sidebar__info-progress">
                        <Text content="Good 742 sales"></Text>
                        <ProgressBar value="55"></ProgressBar>
                    </div>
                <Toggles></Toggles>
            </div>
            <div class="sidebar__info">
                <div class="sidebar__info-user">
                    <UserProfileImg></UserProfileImg>
                    <div class="sidebar__info-name">
                        <Text content="Berkancing"></Text>
                        <Text content="ID: 098134NN"></Text>
                    </div>
                </div>
                    <Text content="$230.98"></Text>
                    <Text content="44"></Text>
                    <div class="sidebar__info-progress">
                        <Text content="Bad 500 sales"></Text>
                        <ProgressBar value="46"></ProgressBar>
                    </div>
                <Toggles></Toggles>
            </div>
            <div class="sidebar__info">
                <div class="sidebar__info-user">
                    <UserProfileImg></UserProfileImg>
                    <div class="sidebar__info-name">
                        <Text content="Berkancing"></Text>
                        <Text content="ID: 098134NN"></Text>
                    </div>
                </div>
                    <Text content="$540.98"></Text>
                    <Text content="555"></Text>
                    <div class="sidebar__info-progress">
                        <Text content="Bad 260 sales"></Text>
                        <ProgressBar value="32"></ProgressBar>
                    </div>
                <Toggles></Toggles>
            </div>
            <div class="sidebar__info">
                <div class="sidebar__info-user">
                    <UserProfileImg></UserProfileImg>
                    <div class="sidebar__info-name">
                        <Text content="Berkancing"></Text>
                        <Text content="ID: 098134NN"></Text>
                    </div>
                </div>
                    <Text content="$410.98"></Text>
                    <Text content="240"></Text>
                    <div class="sidebar__info-progress">
                        <Text content="Bad 120 sales"></Text>
                        <ProgressBar value="19"></ProgressBar>
                    </div>
                <Toggles></Toggles>
            </div>
            <div class="sidebar__info">
                <div class="sidebar__info-user">
                    <UserProfileImg></UserProfileImg>
                    <div class="sidebar__info-name">
                        <Text content="Berkancing"></Text>
                        <Text content="ID: 098134NN"></Text>
                    </div>
                </div>
                    <Text content="$40.98"></Text>
                    <Text content="340"></Text>
                    <div class="sidebar__info-progress">
                        <Text content="Bad 420 sales"></Text>
                        <ProgressBar value="49"></ProgressBar>
                    </div>
                <Toggles></Toggles>
            </div>
          </div>
          <div class="sidebar__row5">
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
import Select from './Select.vue';
import Button from './Button.vue';

import Aimat from './assets/WIN_20231222_04_47_32_Pro.jpg'
import RingPieChart from './RingPieChart.vue';
import ProgressBar from './ProgressBar.vue';
import Toggles from './Toggles.vue';

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
    Pagination,
    Select,
    Button,
    Search,
    ProgressBar,
    Toggles
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
        dropdownOptions: [
        { label: 'Option 1', value: 'option1' },
        { label: 'Option 2', value: 'option2' },
        { label: 'Option 3', value: 'option3' }
        ],
        selectedItem: ''
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
  .sidebar__first{
    display: flex;
    gap:40px;
  }
  .sidebar__row-search-input{
    padding-top: 10px;
  }
  .sidebar__sort{
    display: flex;
  }
  .sidebar__row{
    display: flex;
    justify-content: space-around;
  }
  .sidebar__row2{
    padding-top: 25px;
    display: flex;
    justify-content: space-around;
  }  
  .sidebar__row4{
    display: grid;
  }
  .sidebar__row5{
    display: flex;
    padding-top: 40px;
    padding-left: 110vh;
  }
  .sidebar__info-progress{
    display: block;
  }
  .sidebar__columns{
    display: flex;
    gap:135px;
  }
  .sidebar__info{
    display: flex;
    padding-top: 20px;
    justify-content: space-around;
    align-items: center;
  }
  .sidebar__info-user{
    display: flex;
    align-items: center;
  }
  .sidebar__info-name{
    display: grid;
    padding-left: 20px;
  }

  .sidebar__withIcon{
    display: flex;
    gap: 8px;
  }
  .sidebar__row-filter{
    padding-top: 10px;
    display: flex;
    gap: 10px;
  }
  .sidebar__icons{
    display: flex;
    gap: 5px;
    }
    .sidebar__row3{
        padding-top: 40px;
        display: flex;
        justify-content: space-around;
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
  </style>