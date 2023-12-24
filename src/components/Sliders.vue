<template>
    <div class="container">
        <input type="range" min="0" max="100" @input="updateSliderValue">
        <p>Current Value: {{ currentValue }}</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            currentValue: 50 // Default value for the slider
        };
    },
    methods: {
        updateSliderValue(event) {
            this.currentValue = event.target.value;
        }
    }
}
</script>

<style>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-top: 40px;
}

input[type="range"] {
    width: 300px;
    margin-bottom: 20px;
}

p {
    font-size: 18px;
}
</style>
