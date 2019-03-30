<template>
  <div class="login-box middle">
    <h1>Login</h1>
    <div class="textbox">
      <input type="text" name="username" placeholder="用户名">
    </div>
    <div class="textbox">
      <input type="password" name="password" placeholder="密码">
    </div>
    <input class="btn" type="button" value="登录">
    <a href="#" class="forget">忘记密码?</a>
    <a href="#" class="create">创建账号</a>
  </div>
</template>

<script>
export default {
  name: "LogininForm1",
  activated(){
    this.bg = document.getElementsByTagName('body')[0]
    this.bg.className = 'bg'
  },
  deactivated(){
     this.bg.removeAttribute('class','bg')
  },
  data() {
    return {
      bg:null,
    };
  }
};
</script>

<style scoped lang="scss">
.forget,.create{
  text-decoration: none;
  display:block;
  width: 260px;
   padding: 10px 0;
   margin: auto;
}
 .forget{
   color: white;
   margin-top: 15px;
   
   transform: 0.4s all;
    &:hover{
    background: rgba(51, 51, 51, 0.42);
  }
 }
  .create{
    color: #3498db;
    margin-top: 50px;
    font-size: 20px;
    transform: 0.4s all;
     &:hover{
    background: rgba(51, 51, 51, 0.42);
  }
    
 }
.login-box{
  width: 360px;
  height: 600px;
  color:white;
  text-align: center;
  h1{
   text-transform: uppercase;
   margin-top: 125px;//用ps测的...
   margin-bottom: 60px;
   font-size: 40px;//big
  }
  .btn{
    width: 260px;
    height: 40px;
    background: #2980b9;
    color:white;
    border-radius: 10px;
    border: none;
    margin:  14px auto;//居中
    display: block;
    font-size: 16px;
    cursor: pointer;
  }
  .textbox{
    width: 260px;
    height: 40px;
    margin:  10px auto;
    background: rgba(189, 195, 199,0.8);
    border-radius: 10px;
    input{
      border-radius: 10px;
     text-align: center;
     background: none;
     border: none;
     outline: none;
     width: 100%;
     line-height: 37px;//f12调出来的
     font-size: 14px;
     color:#333;
    }
    
  }
}
</style>
<style lang="scss">
.bg{
  font-family: sans-serif;
  background: url("~@/assets/bg.jpg") no-repeat;
  background-size: cover;
}
</style>

