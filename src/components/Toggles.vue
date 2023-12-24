<template>
    <div class="containerCheck">
        <label class="switch">
            <input type="checkBox" v-model="isChecked" @change="toggleSwitch">
            <span class="slider"></span>
        </label>
    </div>
</template>

<script>
export default {
    data() {
        return {
            isChecked: false
        };
    },
    methods: {
        toggleSwitch() {
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

.switch {
    position: relative;
    display: inline-block;
    width: 60px;
    height: 34px;
}

.switch input{
    opacity: 0;
    width: 0;
    height: 0;
    margin: 0;       
    padding: 0;   
    appearance: none;
}

.switch input:not(:checked) + .slider:before {
    border-radius: 50%;
}

.switch input:checked + .slider:before {
    border-radius: 50%;
}


.slider {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: #ccc;
    transition: .4s;
    border-radius: 34px;
}

.slider:before {
    position: absolute;
    content: "";
    height: 26px;
    width: 26px;
    left: 4px;
    bottom: 4px;
    background-color: white;
    transition: .4s;
}

input:checked + .slider {
    background-color: #2196F3;
}

input:checked + .slider:before {
    transform: translateX(26px);
}

.h4 {
    margin-left: 10px;
}
</style>
