<template>
  <div @MBValue="takeValue">
    <MainFrame></MainFrame>
  </div>
</template>





<script>
import MainFrame from './components/MainFrame'

export default {
  components:{
    MainFrame
  }
}
</script>