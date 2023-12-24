<template>
    <div class="ac__container">
        <div @click="button" :class="question_class">
            {{ item.question }}
        </div>
        <div :class="answer_class">
            {{ item.answer }}
        </div>
    </div>
</template>

<script>
export default{
    props: ['item'],

    data(){
        return{
            answer_class:'ac__answer',
            question_class:'ac__question'
        }
    },

    methods:{
        button(){
            if(this.answer_class == 'ac__answer'){
                this.answer_class = 'ac__answer active'
                this.question_class = 'ac__question active'
            }
            else{
                this.answer_class = 'ac__answer'
                this.question_class = 'ac__question'
            }
        }
    }
}
</script>

<style>
    .ac__question::after{
        content: url(assets/down.svg);
        float: right;
    }
    .ac__question.active::after{
        content: url(assets/up.svg);
        float: right;
    }
    .ac__answer{
        height: 0;
        overflow: hidden;
        transition: 0.4s;
    }
    .ac__answer.active{
        height: 100%;
    }
</style>