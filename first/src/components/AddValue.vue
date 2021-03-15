<template>
    <div>
        <h2>Add Value</h2><br>
        <h3>{{value}}</h3>
        <button v-on:click='AddValue()'>Add value</button>
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
        AddValue(){
            this.value = this.value + 5;
        }
    }
}

</script>