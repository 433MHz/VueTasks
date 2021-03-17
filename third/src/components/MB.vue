<template>
    <div>
        <div><h3>MB convert</h3></div>
        <div id="dataInput"><input type="number" v-model="MBValue"></div>
        <Data></Data>
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
            MBValue: 0
        }
    },
    
    watch:{
        MBValue(){
            this.$emit('MBValue', this.MBValue)
        }
    }
}
</script>

<style>
     #dataInput{
        margin-bottom: 10px;
    }
</style>