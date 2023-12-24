<template>
    <div class="container">
        <input type="file" class="file" placeholder="File">
    </div>
</template>

<script>
    export default{
        data(){
            return{
                file: ''
            }
        }
    }
</script>


<style>
    .container{
        display: flex;
        justify-content: center;
        padding-top: 40px;
    }
</style>
