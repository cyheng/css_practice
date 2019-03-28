<template>
  <div id="app">
    <div class="next" @click="next"></div>
    <keep-alive>
        <component :is="currentCnt"></component>
    </keep-alive>
  </div>
</template>

<script>
import HoverButton from './components/HoverButton.vue'
import test from './components/test.vue'
export default {
  name: 'app',
  components: {
    HoverButton,test
  },
  data(){
    return {
      cntList:[HoverButton,test],
      cur:0
    }
  },
  methods:{
    next(){
       this.cur = (this.cur + 1 ) % this.cntList.length 
    }
  },
  computed:{
    currentCnt(){
      return this.cntList[this.cur]
    }
  }
}
</script>

<style lang="scss">
body{
  margin: 0;
  padding: 0;
  background: #f1f1f1;
}
.next{
  margin: 15px;
  width: 80px;
  height: 40px;
  background: #2ecc71;
  cursor: pointer;
  border-radius: 5px;
  position: relative;
  &::before{
    color:white;
    content: 'next';
    position:absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
  }
}
</style>
