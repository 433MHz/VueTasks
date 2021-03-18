<template>
<div>
    <div id="mainDataContainer">
            <div class="dataContainers">
                <p>TB (TeraBytes) <br>{{values.TB}}</p><br>
                <p>GB (GigaBytes) <br>{{values.GB}}</p><br>
                <p>MB (MegaBytes) <br>{{values.MB}}</p><br>
                <p>KB (KiloBytes) <br>{{values.KB}}</p><br>
                <p>Byte (Bytes) <br>{{values.B}}</p><br>
            </div>
            <div class="dataContainers">
                <p>Tb (TeraBits) <br>{{values.Tb}}</p><br>
                <p>Gb (GigaBits) <br>{{values.Gb}}</p><br>
                <p>Mb (MegaBits) <br>{{values.Mb}}</p><br>
                <p>Kb (KiloBits) <br>{{values.Kb}}</p><br>
                <p>bit (Bits) <br>{{values.b}}</p><br>

            </div>
        </div>
        </div>
</template>

<script>
export default {

    props:[
        'message'
    ],

    data(){
        return{

            values:{
                TB: 0,
                GB: 0,
                MB: 0,
                KB: 0,
                B: 0,

                Tb: 0,
                Gb: 0,
                Mb: 0,
                Kb: 0,
                b: 0
            }
        }
    },

    watch:{
        message(){
            this.values.TB = this.message / 1000000,
            this.values.GB = this.message / 1000,
            this.values.MB = this.message,
            this.values.KB = this.message * 1000,
            this.values.B = this.message * 1000000,

            this.values.Mb = this.message * 8,
            this.values.Tb = this.values.Mb / 1000000,
            this.values.Gb = this.values.Mb / 1000,
            this.values.Kb = this.values.Mb * 1000,
            this.values.b = this.values.Mb * 1000000
        }
    }
   }

</script>

<style>
    .dataContainers{
        width: 250px;
        height: 400px;
        float: left;
    }

    #mainDataContainer{
        width: 500px;
        height: 400px;
        margin: auto;
        border: 2px dotted orangered;
    }
</style>