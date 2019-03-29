<template>
    <div class="hover-btn" :style="size">
      <div class="btn-content">{{content}}</div>
    </div>
</template>

<script>
export default {
  name: 'HoverButton',
  data(){
    return {
        content:'Hover me',
        size:{
           width:'200px',
           height:'60px'
        }
    }
  }
}
</script>

<style scoped lang="scss">
 
 .hover-btn{
   width: 200px;
   height: 60px;
   position: absolute;
   top:50%;
   left: 50%;
   transform: translate(-50%,-50%);
   background: #f39c12;
   cursor: pointer;
   border-radius: 5px;
   overflow: hidden;
   &:hover{
     .btn-content{
        top:-50%;
     }
   }
    &:hover::after{
     top:50%;
   }
  //  文字
   .btn-content{
     color:white;
     font-family: sans-serif;
     font-size: 20px;
     position: absolute;
     top:50%;
     left: 50%;
     transform: translate(-50%,-50%);
     transition: all 0.5s;
   }
  //  爱心
   &::after{
     font-family: "iconfont";
     content: '\e633';
     font-size: 40px;
     color: red;
     position: absolute;
     top:50%;
     left: 50%;
     transform: translate(-50%,-50%);
     top:140%;
     transition: all 0.5s;
   }
    
 }
</style>
