<template>
    <div class="containerBtn">
        <button :style="buttonStyle" @click="handleButtonClick">
            {{ title }}
        </button>
    </div>
</template>

<script>
export default {
    props: {
        title: {
            type: String,
            required: true
        },
        border: {
            type: String,
            default: 'none'
        },
        backgroundColor: {
            type: String,
            default: 'transparent'
        },
        color: {
            type: String,
            default: 'black'
        },
        padding: {
            type: String,
            default: '10px'
        }
    },
    computed: {
        buttonStyle() {
            return {
                border: this.border,
                backgroundColor: this.backgroundColor,
                color: this.color,
                padding: this.padding
            };
        }
    },
    methods: {
        handleButtonClick() {
            this.$emit('button-clicked', this.title);
        }
    }
}
</script>

<style>
.containerBtn {
    display: flex;
}

.containerBtn button {
    /* You can leave this empty if you're styling through props */
}
</style>
