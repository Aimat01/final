<template>
    <div class="containerPassword">
        <div class="password-input">
            <input :type="inputType" class="text" placeholder="Password" v-model="password" @blur="interacted=true">
            <button @click="toggleVisibility">{{ visibilityText }}</button>
        </div>
        <span v-if="isInvalidPassword" class="error-text">Password must contain at least 8 characters</span>
    </div>
</template>

<script>
export default {
    data() {
        return {
            password: '',
            interacted: false,
            showPassword: false
        };
    },
    computed: {
        isInvalidPassword() {
            return this.interacted && this.password.length < 8;
        },
        inputType() {
            return this.showPassword ? 'text' : 'password';
        },
        visibilityText() {
            return this.showPassword ? 'Hide' : 'Show';
        }
    },
    methods: {
        toggleVisibility() {
            this.showPassword = !this.showPassword;
        }
    }
}
</script>

<style>
.containerPassword {
    display: grid;
    justify-content: center;
    justify-items: center;
    padding-top: 40px;
}

.text {
    width: 40vh;
    padding: 7px;
    border-radius: 5px;
}

.password-input {
    display: flex;
    align-items: center;
}

.error-text {
    color: red;
    margin-left: 10px;
}

button {
    margin-left: 10px;
    cursor: pointer;
    padding: 7px 15px;
    border-radius: 5px;
}
</style>
