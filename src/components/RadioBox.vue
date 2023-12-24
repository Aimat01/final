<template>
    <div class="containerCheck">
        <div class="checks" @click="selectOption('option1')">
            <input type="radio" v-model="selectedOption" value="option1">
            <h4>Option 1</h4>
        </div>
        <div class="checks" @click="selectOption('option2')">
            <input type="radio" v-model="selectedOption" value="option2">
            <h4>Option 2</h4>
        </div>
        <div class="checks" @click="selectOption('option3')">
            <input type="radio" v-model="selectedOption" value="option3">
            <h4>Option 3</h4>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            selectedOption: null // Store the currently selected option
        };
    },
    methods: {
        selectOption(option) {
            this.selectedOption = option;
        }
    }
}
</script>

<style>
.containerCheck {
    display: grid;
    justify-content: center;
    padding-top: 40px;
}

.checks {
    display: flex;
    gap: 10px;
    cursor: pointer;
}
</style>
