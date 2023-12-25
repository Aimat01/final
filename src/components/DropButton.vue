<template>
    <div class="dropdown">
      <button 
        @click="toggleDropdown" 
        :style="{ color: buttonColor }"
        class="dropdown-button"
      >
        {{ buttonText }}
        <span class="arrow">&#9662;</span>
      </button>
      <ul v-if="isOpen" class="dropdown-list">
        <li 
          v-for="(option, index) in options" 
          :key="index"
          @click="selectOption(option)"
          class="dropdown-item"
        >
          {{ option }}
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      options: {
        type: Array,
        required: true
      },
      placeholder: {
        type: String,
        default: 'Select an option'
      },
      initialText: {
        type: String,
        default: 'Select an option'
      },
      initialColor: {
        type: String,
        default: 'black'
      }
    },
    data() {
      return {
        isOpen: false,
        buttonText: this.initialText,
        buttonColor: this.initialColor,
        selectedOption: ''
      };
    },
    watch: {
      initialText(value) {
        this.buttonText = value;
      },
      initialColor(value) {
        this.buttonColor = value;
      }
    },
    methods: {
      toggleDropdown() {
        this.isOpen = !this.isOpen;
      },
      selectOption(option) {
        this.selectedOption = option;
        this.buttonText = option; // Update button text to the selected option
        this.isOpen = false;
        this.$emit('selected', option);  // Emitting an event with the selected option
      }
    }
  };
  </script>

<style scoped>
.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-button {
  padding: 10px 10px;
  border: none;
  background-color: #f9f9f9;
  cursor: pointer;
}

.arrow {
  margin-left: 5px;
}

.dropdown-list {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 10;
  border: 1px solid #ccc;
  list-style-type: none;
  padding: 0;
  margin: 0;
  background-color: #fff;
}

.dropdown-item {
  padding: 8px 15px;
  cursor: pointer;
  border-bottom: 1px solid #ccc;
}

.dropdown-item:last-child {
  border-bottom: none;
}
</style>
