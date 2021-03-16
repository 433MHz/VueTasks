<template>
    <div>
        <h2>Minus value</h2><br>
        <h3>{{value}} {{AddEndValue}}</h3>
        <button v-on:click='MinusValue()'>Minus value</button>
    </div>
</template>



<script>
export default {

    data(){
        return{
        value: 0
        }
    },

    methods:{
        MinusValue(){
            this.value = this.value - 5;
        }
    },

    computed:{
        AddEndValue(){
            return ' : value'
        }
    }
}
</script>