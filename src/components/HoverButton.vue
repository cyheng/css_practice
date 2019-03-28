<template>
    <div id="btn">
    </div>
</template>

<script>
export default {
  name: 'HoverButton',
  data(){
    return {

    }
  }
}
</script>

<style scoped lang="scss">
 
 #btn{
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
   &:hover::before{
     top:-30px;
   }
    &:hover::after{
     top:50%;
   }
  //  文字
   &::before{
     color:white;
     font-family: sans-serif;
     font-size: 20px;
     content: 'Hover me';
     position: absolute;
     top:50%;
     left: 50%;
     transform: translate(-50%,-50%);
     transition: all 0.5s;
   }
  //  爱心
   &::after{
     font-family: 'Ionicons';
     content: '\f141';
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
