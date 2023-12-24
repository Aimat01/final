<template>
    <div class="containerEmail">
        <input type="email" class="text" placeholder="Email" v-model="email" @blur="interacted=true">
        <span v-if="isInvalidEmail" class="error-text">Invalid email format</span>
    </div>
</template>

<script>
export default {
    data() {
        return {
            email: '',
            interacted: false
        };
    },
    computed: {
        isInvalidEmail() {
            // Regular expression to validate email
            const regex = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,6}$/;
            return this.interacted && !regex.test(this.email);
        }
    }
}
</script>

<style>
.containerEmail {
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
