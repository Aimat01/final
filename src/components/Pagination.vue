<template>
  <div class="container">
  <div class="pagination">
    <button @click="prevPage" :disabled="currentPage === 1">Prev</button>
    <span>{{ currentPage }}</span>
    <button @click="nextPage" :disabled="currentPage === totalPages">Next</button>
    <select @change="jumpToPage">
      <option v-for="page in totalPages" :key="page">{{ page }}</option>
    </select>
  </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentPage: 1,
      totalPages: 100 // For example
    };
  },
  methods: {
    prevPage() {
      if (this.currentPage > 1) this.currentPage--;
    },
    nextPage() {
      if (this.currentPage < this.totalPages) this.currentPage++;
    },
    jumpToPage(event) {
      this.currentPage = parseInt(event.target.value);
    }
  }
}
</script>
