<template>
<div id="mainDiv">
    <header>
        <div id="title">Data converter</div>
        <div>
        </div>
    </header>

    <nav>
        <button>TB</button><br>
        <button>GB</button><br>
        <button>MB</button><br>
        <button>KB</button><br>
        <button>Bytes</button><br>
        <button>Gbit</button><br>
        <button>Mbit</button><br>
        <button>Kbit</button><br>
        <button>bit</button>

        {{value}}
    </nav>

    <article><MB></MB></article>

</div>
</template>


<script>
import MB from './MB';

export default {
    components:{
        MB
    },

    methods:{
        insertValue(value){
            this.value = value
        }
    },

    data(){
        return{
            value: ''
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