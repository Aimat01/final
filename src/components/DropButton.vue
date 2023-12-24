<template>  
    <div> 
        <div class="containerDrop">
        <div class="buttons__dropdawn"> 
            <button type="button" @click="show = !show" class="buttons__dropdawn-input"> 
                {{ title }} 
            </button>  
            <a v-if="show" class="buttons__dropdawn-link" v-for="(link , index) in links" :href="link">link {{ index  }}</a> 
        </div> 
        </div>
    </div> 
</template> 
 
<script> 
    export default {  
        data() {  
            return {  
                show: false  
            } 
        }, 
        props: ['title' , 'links'] 
    } 
</script> 
 
<style> 
    .containerDrop{
        display: flex;
        padding-left: 5px;
    }
    .buttons__dropdawn-input{    
       margin-left: 0 ;  
       border: none; 
       color: black; 
       cursor: pointer ;  
       overflow: hidden ;     
       font-family: sans-serif ;     
       margin-bottom: 0px ;    
    } 
 
    .buttons__dropdawn-link{ 
        display: block ;  
        text-decoration: none ; 
        color:  black;  
        width: 136px ;  
        padding: 5px 16px;
        font-size: 14px;  
    } 
 
 
</style>