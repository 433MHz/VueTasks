<template>
  <div>
    <div class="merged">
      <AddValue></AddValue>
    </div>
    <div class="merged">
      <MinusValue></MinusValue>
    </div>
    <div class="merged">
      <List></List>
    </div>
  </div>
</template>



<script>
import AddValue from './AddValue';
import MinusValue from './MinusValue';
import List from './List';

export default {
  components:{
    AddValue,
    MinusValue,
    List
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