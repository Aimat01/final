<template>
    <div class="container">
        <button @click="handleButtonClick('Button 1')">Button 1</button>
        <button @click="handleButtonClick('Button 2')">Button 2</button>
        <button @click="handleButtonClick('Button 3')">Button 3</button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            clickedButton: null
        };
    },
    methods: {
        handleButtonClick(buttonName) {
            this.clickedButton = buttonName;
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
</style>
