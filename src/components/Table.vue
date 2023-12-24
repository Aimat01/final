<template>
  <div class="container">
  <div class="table-container">
    <table class="custom-table">
      <thead>
        <tr>
          <th v-for="(header, index) in headers" :key="index">{{ header }}</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(row, rowIndex) in rows" :key="rowIndex" :class="{ 'even-row': rowIndex % 2 === 0, 'odd-row': rowIndex % 2 !== 0 }">
          <td 
            v-for="(cell, cellIndex) in row" 
            :key="cellIndex"
            :style="{ color: getCellColor(cell) }"
          >
            {{ cell }}
          </td>
        </tr>
      </tbody>
    </table>
  </div>
  </div>
</template>

<script>
export default {
props: {
  headers: {
    type: Array,
    required: true,
  },
  rows: {
    type: Array,
    required: true,
  },
},
methods: {
  getCellColor(value) {
    if (value.toLowerCase() === 'paid') {
      return '#1172d9';
    } else if (value.toLowerCase() === 'unpaid') {
      return '#d91139';
    }else if(value.toLowerCase() === 'unfulfilled'){
      return '#1172d9';
    }else if(value.toLowerCase() === 'cancelled'){
      return '#d9ae11';
    }
    // Add more conditions if needed
    return 'inherit'; // Default color
  },
},
};
</script>

<style scoped>
/* Modern component-specific styles */
.container{
display: grid;
justify-content: center;
padding-top: 40px;
}
.table-container {
width: 100%;
overflow-x: auto;
}

.custom-table {
width: 100%;
border-collapse: collapse;
margin-top: 20px;
}

th, td {
border: none;
padding: 16px;
text-align: left;
}

th {
color: rgb(128, 128, 128);
}

.even-row {
color: black;
}

.odd-row {
color: black;
}
</style>
