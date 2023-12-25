<template>
    <select v-model="selectedValue" @change="handleChange">
      <option value="" disabled selected>{{ text }}</option> <!-- Default text -->
      <option v-for="option in options" :key="option.value" :value="option.value">
        {{ option.label }}
      </option>
    </select>
  </template>
  
  <script>
  export default {
    props: {
      options: {
        type: Array,
        required: true,
        default: () => []
      },
      value: {
        type: [String, Number],
        default: ''
      },
      text:{
        type: String,  
      }
    },
    data() {
      return {
        selectedValue: this.value
      };
    },
    watch: {
      value(newVal) {
        this.selectedValue = newVal;
      }
    },
    methods: {
      handleChange(event) {
        this.$emit('update:value', event.target.value);
      }
    }
  };
  </script>
  
  <style>
  select{
    border: none;
    font-weight: 700;
  }
</style>