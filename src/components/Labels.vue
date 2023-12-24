<template>
    <div class="container">
        <div class="all" @click="clickOn">
            <div class="bd" >
                <div class="" v-html="label">    
                </div>
            <div class="badge">
                0
            </div>
            </div>
        </div>
    </div>
</template>


<script>
export default{
    props:{
        value:{
            value:String,
            default:"0"
        },
        label:String,
    },
    data(){
        return{
            data:"",
        }
      
    },
    methods:{
        clickOn(){
        }
    }
}

</script>

<style scoped>
.container{
        display: flex;
        justify-content: center;
        padding-top: 40px;
    }
.all {
    font-size: 20px;
    font-family: 'Roboto', sans-serif;
    position: relative;
}

.bd {
    position: relative;
    width: 20px;
    color: gray;
}

.badge {
    font-size: 16px;
    position: absolute;
    background-color: #198568;
    color: #fff;
    width: 18px;
    height: 18px;
    border-radius: 50%;
    top: -6px;
    right: -28px;
    display: flex;
    align-items: center;
    justify-content: center; /* This centers the content vertically and horizontally */
}
</style>
