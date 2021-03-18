<template>
    <div>
        <div><h3>MB (MegaBytes) convert</h3></div>
        <div id="dataInput"><input type="number" v-model="MBValue"></div>
        <Data :message="CalculatedValue"></Data>
    </div>
</template>

<script>
import Data from './Data'

export default {

    components:{
        Data
    },

    data(){
        return{
            MBValue: Number,
        }
    },

    computed:{
        CalculatedValue(){
            return this.MBValue;
        }
    }
}
</script>

<style>
     #dataInput{
        margin-bottom: 10px;
    }
</style>