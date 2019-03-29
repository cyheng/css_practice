<template>
  <div id="app">
    <div class="next" @click="next"></div>
    <keep-alive>
        <component :is="currentCnt"></component>
    </keep-alive>
  </div>
</template>

<script>
const components = require.context('./components/', false, /\.vue/)
const items = components.keys().map(x => components(x)).map(x=>x.default)
export default {
  name: 'app',
  data(){
    return {
      cntList:items,
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
    },
     
  }
}
</script>

<style lang="scss">
body{
  margin: 0;
  padding: 0;
  background: #f1f1f1;
}
.middle{
  position: absolute;
  top:50%;
  left: 50%;
  transform: translate(-50%,-50%);
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
