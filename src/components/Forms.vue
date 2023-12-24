<template>
    <div class="container">
        <form @submit.prevent="submitForm">
            <div class="form-group">
                <label for="name">Name:</label>
                <input type="text" id="name" v-model="formData.name" required>
            </div>
            <div class="form-group">
                <label for="email">Email:</label>
                <input type="email" id="email" v-model="formData.email" required>
            </div>
            <div class="form-group">
                <label for="message">Message:</label>
                <textarea id="message" rows="4" v-model="formData.message" required></textarea>
            </div>
            <button type="submit">Submit</button>
        </form>
    </div>
</template>

<script>
export default {
    data() {
        return {
            formData: {
                name: '',
                email: '',
                message: ''
            }
        };
    },
    methods: {
        submitForm() {
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

.form-group {
    margin-bottom: 20px;
}

label {
    display: block;
    margin-bottom: 8px;
}

input[type="text"],
input[type="email"],
textarea {
    width: 300px;
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 4px;
}
</style>
