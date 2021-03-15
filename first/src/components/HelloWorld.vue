<template>
  <div>
    <div class="merged">
      <AddValue></AddValue>
    </div>
    <div class="merged">
      <MinusValue></MinusValue>
    </div>
  </div>
</template>



<script>
import AddValue from './AddValue';
import MinusValue from './MinusValue';

export default {
  components:{
    AddValue,
    MinusValue
  }
}
</script>



<style>
  .merged{
    float: left;
    border: 1px solid gray;
    padding: 30px;
  }

  body{
    text-align: center;
  }
</style>