<template>
    <div class="containerCheck">
        <div class="checks" @click="toggleCheckbox('option1')">
            <input type="checkbox" v-model="option1">
            <h4>Option 1</h4>
        </div>
        <div class="checks" @click="toggleCheckbox('option2')">
            <input type="checkbox" v-model="option2">
            <h4>Option 2</h4>
        </div>
        <div class="checks" @click="toggleCheckbox('option3')">
            <input type="checkbox" v-model="option3">
            <h4>Option 3</h4>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            option1: false,
            option2: false,
            option3: false
        };
    },
    methods: {
        toggleCheckbox(option) {
            this[option] = !this[option]; // Toggle the specific checkbox state
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
