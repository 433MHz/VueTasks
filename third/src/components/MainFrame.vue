<template>
<div id="mainDiv">
    <header>
        <div id="title">Data converter</div>
        <div>
        </div>
    </header>

    <nav>
        <button v-on:click="SwitchComponent('TB')">TB</button><br>
        <button v-on:click="SwitchComponent('GB')">GB</button><br>
        <button v-on:click="SwitchComponent('MB')">MB</button><br>
        <button v-on:click="SwitchComponent('KB')">KB</button><br>
        <button v-on:click="SwitchComponent('B')">Bytes</button><br>
        <button v-on:click="SwitchComponent('Gbit')">Gbit</button><br>
        <button v-on:click="SwitchComponent('Mbit')">Mbit</button><br>
        <button v-on:click="SwitchComponent('Kbit')">Kbit</button><br>
        <button v-on:click="SwitchComponent('bit')">bit</button>
    </nav>

    <article><component v-bind:is="component"></component></article>

</div>
</template>


<script>
import MB from './MB';
import TB from './TB';

export default {
    components:{
        MB,
        TB
    },

    methods:{
        SwitchComponent(com){
            this.component = com
        }
    },

    data(){
        return{
            component: MB
        }
    }
}
</script>


<style>
    #mainDiv{
        width: 1000px;
        margin: auto;
    }

    body{
        margin: 0;
        background-color: rgb(238, 238, 238);
    }

    header{
        background-color: burlywood;
        width: 1000px;
        height: 80px;
    }

    nav{
        margin-top: 20px;
        padding-top: 5px;
        padding-bottom: 50px;
        background-color: burlywood;
        width: 250px;
        height: 500px;
        text-align: center;
        font-size: 20px;
        float: left;
    }

    nav button{
        width: 90%;
        height: 50px;
        margin-top: 5px;
    }

    #title{
        font-size: 30px;
        text-align: center;
    }

    article{
        float: left;
        background-color: burlywood;
        margin-left: 20px;
        margin-top: 20px;
        width: 730px;
        height: 560px;
        text-align: center;
    }
</style>