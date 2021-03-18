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
        <button v-on:click="SwitchComponent('Tbit')">Tbit</button><br>
        <button v-on:click="SwitchComponent('Gbit')">Gbit</button><br>
        <button v-on:click="SwitchComponent('Mbit')">Mbit</button><br>
        <button v-on:click="SwitchComponent('Kbit')">Kbit</button><br>
        <button v-on:click="SwitchComponent('bit')">bit</button>
    </nav>

    <article><component v-bind:is="component"></component></article>

</div>
</template>


<script>
import TB from './TB';
import GB from './GB';
import MB from './MB';
import KB from './KB';
import B from './B';

import Tbit from './Tbit';
import Gbit from './Gbit';
import Mbit from './Mbit';
import Kbit from './Kbit';
import bit from './bit';

export default {
    components:{
        TB,
        GB,
        MB,
        KB,
        B,
        Tbit,
        Gbit,
        Mbit,
        Kbit,
        bit
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
        height: 530px;
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
        height: 585px;
        text-align: center;
    }
</style>