<template>
    <div class="image middle">
      <img src="@/assets/img.jpg" alt="">
      <div class="image-content">
        <h1>image Title</h1>
        <div class="icons">
          <a href="#" class="icon iconfont icon-heart"></a>
          <a href="#" class="icon  iconfont icon-comment"></a>
          <a href="#" class="icon  iconfont icon-share"></a>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'ImageHover',
  data(){
    return {
         
    }
  }
}
</script>

<style scoped lang="scss">
.image{
  width: 440px;
  height: 300px;
  overflow: hidden;
  cursor: pointer;
  &:hover .image-content h1,&:hover .icon{
    transform: translateY(0px);
  }
}
.image-content{
  position:absolute;
  top:0;
  left: 0;
  width: 100%;
  height: 100%;
  padding: 40px;
  box-sizing: border-box;
  h1{
    color:#fff;
    text-transform: uppercase;
    transform: translateY(20px);
    transition: 0.4s;
  }
  &::before{
    content: "";
    position: absolute;
    left: 0;
    bottom: 0;
    background: rgba(255,255,255,0.7);
    width: 100%;
    height: 0px;
    clip-path: polygon(0 100%,100% 0,100% 100%);//3个点 左下角 右上角 右下角
    transition: 0.5s;
  }
  &:hover::before{
    height: 140px;
  }
}
.icons{
  position:absolute;
  right: 40px;
  bottom: 40px;
  .icon{
    text-decoration: none;
    color:#333;
    font-size: 22px;
    margin:0 10px;
    transform: translateY(80px);
    display: inline-block;
    &:nth-child(1){
      transition: transform 0.4s 0.05s,color 0.4s;
    }
     &:nth-child(2){
      transition: transform 0.4s 0.1s,color 0.4s;
    }
     &:nth-child(3){
      transition: transform 0.4s 0.15s,color 0.4s;
    }
    &:hover{
      color:#3498db;
    }
  }
}
</style>
