<template>
  <div class="pagination">
    <img src="https://cdn-icons-png.flaticon.com/128/271/271220.png" width="15px" @click="previousPage" :disabled="currentPage === 1">
    
    <!-- Display page numbers -->
    <div class="page-numbers">
      <span 
        v-for="page in pagesToShow" 
        :key="page"
        @click="goToPage(page)"
        :class="{ 'active': currentPage === page }"
      >
        {{ page }}
      </span>
    </div>
    
    <img src="https://cdn-icons-png.flaticon.com/128/271/271228.png" width="15px" @click="nextPage" :disabled="currentPage === totalPages">
  </div>
</template>

<script>
export default {
  props: {
    totalItems: {
      type: Number,
      required: true
    },
    itemsPerPage: {
      type: Number,
      default: 10
    },
    pagesToShow: {
      type: Number,
      default: 7 // Number of pages to show in the pagination
    }
  },
  data() {
    return {
      currentPage: 1
    };
  },
  computed: {
    totalPages() {
      return Math.ceil(this.totalItems / this.itemsPerPage);
    }
  },
  methods: {
    nextPage() {
      if (this.currentPage < this.totalPages) {
        this.currentPage++;
      }
    },
    previousPage() {
      if (this.currentPage > 1) {
        this.currentPage--;
      }
    },
    goToPage(page) {
      this.currentPage = page;
    }
  }
};
</script>

<style scoped>
.pagination {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 20px;
}

.page-numbers span {
  margin: 0 5px;
  cursor: pointer;
}

.page-numbers span.active {
  font-weight: bold;
}
</style>
