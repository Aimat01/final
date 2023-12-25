<template>
    <div class="sidebar">
      <div class="sidebar-header">
        <div class="sidebar__column">
          <div class="sidebar__tanda">
            <div class="sidebar__row-order">
              <Icons src="https://cdn-icons-png.flaticon.com/128/271/271220.png"></Icons>
              <Text content="Order Details"></Text>
            </div>
            <div class="sidebar__row-order2">
              <div class="sidebar__row-order">
                <Icons src="https://cdn-icons-png.flaticon.com/128/3022/3022251.png"></Icons>
                <Text content="Print order"></Text>
              </div>
              <div class="sidebar__row-order">
                <Icons src="https://cdn-icons-png.flaticon.com/128/2947/2947554.png"></Icons>
                <Text content="Refund items"></Text>
              </div>
              <div class="sidebar__row-order">
                <!-- <Text content="More Actions"></Text>
                <Icons src="https://cdn-icons-png.flaticon.com/128/32/32195.png"></Icons> -->
                  <DropButton initialText="More actions" :options="options"></DropButton>
              </div>
            </div>
          </div>
          <div class="sidebar__two">
            <div class="sidebar__yourInfo">
              <div class="sidebar__yourInfo-status">
                <Icons src="https://cdn-user-icons.flaticon.com/123098/123098580/1703494069049.svg?token=exp=1703494971~hmac=b9d3ace914d80bec1ad01676d3611991"></Icons>
                <Text content="Unfulfilled" color="red"></Text>
              </div>
              <div class="sidebar__info">
                <div class="sidebar__info-user">
                    <UserProfileImg></UserProfileImg>
                    <div class="sidebar__info-name">
                        <Text content="Pattern top with knot" fontWeight="700"></Text>
                        <Text content="ID: 098134NN"></Text>
                    </div>
                </div>
                <div class="sidebar__info-balance">
                  <Text content="$500.98" fontWeight="700"></Text>
                  <Text content="Qty: 1" color="gray"></Text>
                </div>
              </div>
              <div class="sidebar__button">
                <Button color="blue" title="Mark as fulfilled"></Button>
                <Button backgroundColor="blue" title="Crate shipping label" color="white"></Button>
              </div>
              <div class="sidebar__paid">
                <Icons src="https://cdn-user-icons.flaticon.com/123098/123098580/1703496134139.svg?token=exp=1703497035~hmac=200d1acbfe1da627c6cbc0113d8305b8"></Icons>
                <Text content="Paid" color="blue"></Text>
              </div>
              <div class="sidebar__costs">
                <div class="sidebar__costs-row">
                  <Text content="Subtotal"></Text>
                  <Text content="1 Item" color="gray"></Text>
                  <Text content="$210.98"></Text>
                </div>
                <div class="sidebar__costs-row">
                  <Text content="Shipping"></Text>
                  <Text content="AU Standard Delivery (100kg)" color="gray"></Text>
                  <Text content="$210.98"></Text>
                </div>
                <div class="sidebar__costs-row">
                  <Text content="Tax"></Text>
                  <Text content="GST (AU) 10%" color="gray"></Text>
                  <Text content="$10.15"></Text>
                </div>
                <div class="sidebar__costs-row-total">
                  <Text content="Total" fontWeight="700"></Text>
                  <Text content="$2.75" fontWeight="700"></Text>
                </div>
              </div>
              <div class="sidebar__byCustomer">
                <Text content="Paid by customer"></Text>
                <Text content="$223.88" fontWeight="700" fontSize="20px"></Text>
              </div>
            </div>
            <div class="sidebar__customerInfo">
              <div class="sidebar__customer-text">
                <Text content="Customer" font-weight="700" font-size="20px"></Text>
              </div>
              <div class="sidebar__info-user">
                    <UserProfileImg shape="circle"></UserProfileImg>
                    <div class="sidebar__info-name">
                        <Text content="Aimat Kulmakhan" fontWeight="700"></Text>
                        <Text content="10 orders"></Text>
                    </div>
                    <Icons src="https://cdn-icons-png.flaticon.com/128/5162/5162113.png" style="padding-left: 70px;"></Icons>
                </div>
                <div class="sidebar__info-contact">
                  <div class="sidebar__info-contact-name">
                      <Text content="Contact Information" font-weight="700"></Text>
                      <Button title="Edit" color="blue"></Button>
                  </div>
                  <div class="sidebar__info-contact-inputs">
                    <div class="sidebar__info-contact-email">
                      <Icons src="https://cdn-icons-png.flaticon.com/128/2512/2512053.png"></Icons>  
                      <EmailInput></EmailInput>
                    </div>
                    <div class="sidebar__info-contact-email">
                      <Icons src="https://cdn-icons-png.flaticon.com/128/4083/4083631.png"></Icons>
                      <NumberInput></NumberInput>
                    </div>
                  </div>
                </div>
                <div class="sidebar__info-contact">
                  <div class="sidebar__info-contact-name">
                      <Text content="Shipping Address" font-weight="700"></Text>
                      <Button title="Edit" color="blue"></Button>
                  </div>
                  <div class="sidebar__info-contact-inputs">
                    <div class="sidebar__info-contact-email">
                      <Icons src="https://cdn-icons-png.flaticon.com/128/2512/2512053.png"></Icons>  
                      <TextInput></TextInput>
                    </div>
                  </div>
                </div>
                <div class="sidebar__info-contact">
                  <div class="sidebar__info-contact-name">
                      <Text content="Billing Address" font-weight="700"></Text>
                      <Button title="Edit" color="blue"></Button>
                  </div>
                  <div class="sidebar__info-contact-inputs">
                    <div class="sidebar__info-contact-email">
                      <Icons src="https://cdn-icons-png.flaticon.com/128/2512/2512053.png"></Icons>  
                      <TextInput></TextInput>
                    </div>
                  </div>
                </div>
            </div>
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
import TextInput from './TextInput.vue'

import Aimat from './assets/WIN_20231222_04_47_32_Pro.jpg'
import RingPieChart from './RingPieChart.vue';
import ProgressBar from './ProgressBar.vue';
import Toggles from './Toggles.vue';
import MessageBox from './MessageBox.vue';
import EmailInput from './EmailInput.vue';
import NumberInput from './NumberInput.vue';

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
    Toggles,
    MessageBox,
    EmailInput,
    NumberInput,
    TextInput
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
        selectedItem: '',
        options:[
          'Option 1',
          'Option 2', 
          'Option 3'
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
  .sidebar__button{
    padding-top: 60px;
    padding-left: 57vh;
    gap: 20px;
    display: flex;
  }
  .sidebar__info-user{
    padding-top: 20px;
    display: flex;
    justify-content: space-between;
  }
  .sidebar__info-contact{
    padding-top: 30px;
  }
  .sidebar__info-contact-name{
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .sidebar__info-contact-email{
    padding-top: 20px;
    display: flex;
    gap: 5px;
  }
  .sidebar__customerInfo{
    padding-top: 20px;
    padding-left: 80px;
  }
  .sidebar__paid{
    display: flex;
    align-items: center;
    gap: 20px;
    padding-left: 40px;
    padding-top: 40px;
  }
  .sidebar__costs{
    padding-left: 40px;
    padding-top: 40px;
  }
  .sidebar__two{
    display: flex;
  }
  .sidebar__costs-row{
    display: flex;
    justify-content: space-between;
    padding-top: 10px;
    max-width: 93vh;
  }
  .sidebar__costs-row-total{
    padding-top: 10px;
    max-width: 93vh;
    display: flex;
    justify-content: space-between;
  }
  .sidebar__byCustomer{
    padding-top: 30px;
    padding-left: 40px;
    display: flex;
    justify-content: space-between;
    max-width: 99vh;
    align-items: center;
  }
  .sidebar__first{
    display: flex;
    gap:40px;
  }
  .sidebar__row-order{
    display: flex;
    align-items: center;
    gap: 7px;
  }
  .sidebar__info-balance{
    display: grid;
  }
  .sidebar__row-order2{
    display: flex;
    gap: 50px;
  }
  .sidebar__yourInfo{
    display: block;
  }
  .sidebar__yourInfo-status{
    display: flex;
    align-items: center;
    gap: 15px;
    padding-top: 20px;
    padding-left: 33px;
  }
  .sidebar__row-search-input{
    padding-top: 10px;
  }
  .sidebar__sort{
    display: flex;
  }
  .sidebar__tanda{
    padding-left: 30px;
    display: flex;
    gap: 75vh;
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
    padding-left: 45px;
    gap: 50vh;
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
  .sidebar__column-big{
    display: grid;
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
    justify-content: space-between;
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