<template>
    <div class="containerNumber">
        <input type="text" class="text" placeholder="Number" v-model="number" @blur="interated=true">
        <!-- Call the validation function on input change -->
        <span v-if="invalidInput" class="error-text">Invalid number</span>
    </div>
</template>

<script>
export default {
    data() {
        return {
            number: '',
            interated: false
        };
    },
    computed: {
        invalidInput() {
            // Regular expression to check for invalid symbols
            const regex = /^[0-9]+(\.[0-9]+)?$/;
            return this.interated && !regex.test(this.number);
        }
    }
}
</script>

<style>
.containerNumber {
    display: grid;
    justify-content: center;
    padding-top: 40px;
}

.text {
    width: 40vh;
    padding: 7px;
    border-radius: 5px;
}

.error-text {
    color: red;
    margin-left: 10px; 
    /* Add some spacing to the left of the text */
}
</style>
