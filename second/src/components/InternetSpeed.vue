<template>
<div id="mainFrame">
    <h1>Megabits conversion</h1>

    <div id="convertType">
        <button v-on:click="buttonCall(1)" v-bind:class='{choosed: buttonClicked.button1}'>Mb</button>
        <button v-on:click="buttonCall(2)" v-bind:class='{choosed: buttonClicked.button2}'>Kb</button>
        <button v-on:click="buttonCall(3)" v-bind:class='{choosed: buttonClicked.button3}'>b</button>
        <button v-on:click="buttonCall(4)" v-bind:class='{choosed: buttonClicked.button4}'>MB</button>
        <button v-on:click="buttonCall(5)" v-bind:class='{choosed: buttonClicked.button5}'>KB</button>
        <button v-on:click="buttonCall(6)" v-bind:class='{choosed: buttonClicked.button6}'>B</button>
    </div>

<div id="input"><label for="dataInput">Insert value: </label><input name="dataInput" type="number" v-model="currentValue"></div>

<div id="leftDataInputs">
    <label for="mbit">Mb: </label><input name="mbit" type="text" v-model="tempValues.Mbit"><br>
    <label for="kbit">Kb: </label><input name="kbit" type="text" v-model="tempValues.Kbit"><br>
    <label for="bits">b: </label><input name="bits" type="text" v-model="tempValues.Bit"><br>
</div>

<div id="rightDataInputs">
    <label for="mbyte">MB: </label><input name="mbyte" type="text" v-model="tempValues.Mbyte"><br>
    <label for="kbyte">KB: </label><input name="kbyte" type="text" v-model="tempValues.Kbyte"><br>
    <label for="byte">B: </label><input name="byte" type="text" v-model="tempValues.Byte"><br>
</div>
<div style="clear: both"></div>
<div id="bottomButtonDiv">
</div>
</div>
</template>


<style>
#mainFrame{
    border: 1px solid gray;
    width: 700px;
    height: 1000px;
    text-align: center;
}

#leftDataInputs{
    width: 300px;
    text-align: right;
    float: left;
}

#rightDataInputs{
    width: 300px;
    text-align: right;
    float: left;
}

#bottomButtonDiv{
    margin-top: 30px;
    width: 700px;
    text-align: center;
}

#convertType{
    width: 700px;
    height: 100px;
}

#convertType button{
    float: left;
    background-color: aliceblue;
    width: 116.5px;
    height: 30px;
}

#input{
    margin-bottom: 30px;
}

.choosed{
    background-color: aquamarine !important;
    width: 100px;
}
</style>


<script>
export default {
    data(){
        return{
            currentValue: 0,
            clicked: 0,
            buttonClicked:{
                button1: false,
                button2: false,
                button3: false,
                button4: false,
                button5: false,
                button6: false
            },

            tempValues:{
            Mbit: 0,
            Mbyte: 0,
            Kbit: 0,
            Kbyte: 0,
            Bit: 0,
            Byte: 0
            }

        }
    },

    methods:{
       CalculateValues(){

       },

       buttonCall(number){

            this.buttonClicked.button1 = false;
            this.buttonClicked.button2 = false;
            this.buttonClicked.button3 = false;
            this.buttonClicked.button4 = false;
            this.buttonClicked.button5 = false;
            this.buttonClicked.button6 = false;



           switch (number) {
                case 1:
                    this.buttonClicked.button1 = true;
                    this.clicked = 1;
                   break;

                case 2:
                    this.buttonClicked.button2 = true;
                    this.clicked = 2;
                   break;

                case 3:
                    this.buttonClicked.button3 = true;
                    this.clicked = 3;
                   break;

                case 4:
                    this.buttonClicked.button4 = true;
                    this.clicked = 4;
                   break;

                case 5:
                    this.buttonClicked.button5 = true;
                    this.clicked = 5;
                   break;

                case 6:
                    this.buttonClicked.button6 = true;
                    this.clicked = 6;
                   break;
           }
       },

       makeSomeMath(){
           switch (this.clicked) {
                case 1:
                    this.tempValues.Bit = this.currentValue * 1000000;
                    break;

                case 2:
                    this.tempValues.Bit = this.currentValue * 1000;
                    break;

                case 3:
                    this.tempValues.Bit = this.currentValue;
                    break;

                case 4:
                    this.tempValues.Bit = (this.currentValue / 8) * 1000000;
                    break;

                case 5:
                    this.tempValues.Bit = (this.currentValue / 8) * 1000;
                    break;

                case 6:
                    this.tempValues.Bit = this.currentValue / 8;
                    break;
            }

            this.tempValues.Mbit = this.tempValues.Bit / 1000000;
            this.tempValues.Kbit = this.tempValues.Bit / 1000;
            this.tempValues.Byte = this.tempValues.Bit / 8;
            this.tempValues.Mbyte = (this.tempValues.Bit / 8) / 1000000;
            this.tempValues.Kbyte = (this.tempValues.Bit / 8) / 1000;
       }
    },

    watch:{
        currentValue(){
            this.makeSomeMath();
        },

        clicked(){
            this.makeSomeMath();
        }
    },

    computed:{

    }
}
</script>