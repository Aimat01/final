<template>
    <div class="containerArea">
        <textarea placeholder="Write Something" v-model="area" class="textArea"></textarea>
    </div>
</template>

<script>
export default {
    data() {
        return {
            area:''
        };
    }
}
</script>

<style>
.containerArea {
    display: grid;
    justify-content: center;
    padding-top: 40px;
}

.textArea {
    width: 40vh;
    height: 10vh;
    padding: 7px;
    border-radius: 5px;
}
</style>
