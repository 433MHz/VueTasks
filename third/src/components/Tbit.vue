<template>
    <div>
        <div><h3>Tb (TeraBits) convert</h3></div>
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
            return this.MBValue * 1000000 / 8
        }
    }
}
</script>

<style>
     #dataInput{
        margin-bottom: 10px;
    }
</style>