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
    </nav>

    <article>Lorem ipsum</article>

</div>
</template>



<style>
    #mainDiv{
        width: 60%;
        height: 700px;
        margin: auto;
    }

    body{
        margin: 0;
        background-color: rgb(238, 238, 238);
    }

    header{
        background-color: burlywood;
        width: 100%;
        height: 80px;
    }

    nav{
        margin-top: 20px;
        padding-top: 5px;
        padding-bottom: 50px;
        background-color: burlywood;
        width: 250px;
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
        width: 75%;
    }
</style>