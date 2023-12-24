<template>
    <div class="container">
        <select v-model="select">
            <option v-for="select in selects">{{ select }}</option>
        </select>
    </div>
</template>

<script>
    export default{
        data(){
            return{
                select: '',
                selects:['Kazakhstan', 'Uzbekistan', 'South Korea', 'Germany']
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
    .text{
        width: 40vh;
        padding: 7px;
        border-radius: 5px;
    }
</style>