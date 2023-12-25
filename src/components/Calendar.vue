<template>
    <div class="calendar">
      <div class="header">
        <span class="currentMonth">{{ currentMonth }}</span>
      </div>
      <div class="week-days">
        <div class="week-day" v-for="day in weekDays" :key="day">{{ day }}</div>
      </div>
      <div class="days">
        <div 
          class="day" 
          v-for="day in daysInMonth" 
          :key="day" 
          :class="{ 'day-blue': isSelected(day) }"
          @click="selectDay(day)">
          {{ day }}
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        date: new Date(),
        weekDays: ['Su', 'Mo', 'Tu', 'We', 'Th', 'Fr', 'Sa'],
        selectedDay: null
      };
    },
    computed: {
      currentMonth() {
        const options = { month: 'long', year: 'numeric' };
        return this.date.toLocaleDateString('en-US', options);
      },
      daysInMonth() {
        const totalDays = new Date(this.date.getFullYear(), this.date.getMonth() + 1, 0).getDate();
        return Array.from({ length: totalDays }, (_, i) => i + 1);
      },
    },
    methods: {
      selectDay(day) {
        this.selectedDay = day;
      },
      isSelected(day) {
        return this.selectedDay === day;
      }
    }
  };
  </script>
  
  <style scoped>
  .calendar {
    font-family: Arial, sans-serif;
  }
  
  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px;
    background-color: #f2f2f2;
  }
  
  .currentMonth{
    font-weight: 700;
    margin-left: -10px;
    font-size: 12px;
  }

  .day-blue {
    background-color: blue;
    opacity: 0.7;
    color: white; /* Optional: To ensure the number is visible against the blue background */
    }

  .week-days {
  display: grid;
  grid-template-columns: repeat(7, 1fr);
  gap: 10px;
  padding: 10px;
  background-color: #f2f2f2;
  font-weight: bold;
}

  .days {
    display: grid;
    grid-template-columns: repeat(7, 1fr);
    gap: 10px;
    padding: 10px;
    cursor: pointer;
  }
  
  .day {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 40px;
    height: 40px;
    border-radius: 10px;
  }
  </style>
  