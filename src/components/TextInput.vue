<template>
    <div class="containerText">
        <input type="text" class="text" placeholder="Name" v-model="name" @blur="interacted = true">
         <!-- Update the interacted state on blur -->
        <span v-if="showError" class="error-text">require</span>
    </div>
</template>

<script>
export default {
    data() {
        return {
            name: '',
            interacted: false // Track if the input has been interacted with
        };
    },
    computed: {
        showError() {
            return this.interacted && !this.name.trim(); // Display error only if interacted and empty
        }
    }
}
</script>

<style>
.containerText {
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
