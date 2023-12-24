<template>
    <div class="container">
        <input type="datetime-local" class="text" placeholder="Name" v-model="name">
    </div>
</template>

<script>
import { customRef } from 'vue';

export default {
    data() {
        return {
            name: this.getCurrentDateTime() // Set the default value to the current date and time
        };
    },
    methods: {
        getCurrentDateTime() {
            const now = new Date();
            const year = now.getFullYear();
            const month = String(now.getMonth() + 1).padStart(2, '0'); // Months are 0-indexed
            const day = String(now.getDate()).padStart(2, '0');
            const hours = String(now.getHours()).padStart(2, '0');
            const minutes = String(now.getMinutes()).padStart(2, '0');

            return `${year}-${month}-${day}T${hours}:${minutes}`;
        }
    }
}
</script>

<style>
.container {
    display: flex;
    justify-content: center;
    padding-top: 40px;
}

.text {
    width: 40vh;
    padding: 7px;
    border-radius: 5px;
}
</style>
