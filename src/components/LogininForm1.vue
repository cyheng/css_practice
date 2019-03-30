<template>
  <div class="login-box middle">
    <h1>Login</h1>
    <div class="textbox">
      <i class="iconfont icon-user"></i>
      <input type="text" name="username" placeholder="用户名">
    </div>
    <div class="textbox">
      <i class="iconfont icon-password"></i>
      <input type="password" name="password" placeholder="密码">
    </div>
    <input class="btn" type="button" value="登录">
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
.login-box{
  width: 280px;
  color:white;
  h1{
    float: left;
    font-size: 40px;
    border-bottom: 6px solid #4caf50;
    margin-bottom: 50px;
    padding: 13px 0;
  }
  .btn{
    width: 100%;
    background: #4caf50;
    border: 2px solid #4caf50;
    color: white;
    padding: 5px;
    font-size: 18px;
    cursor: pointer;
    margin: 12px 0;
  }
  .textbox{
    width: 100%;
    overflow: hidden;
    font-size: 20px;
    padding: 8px 0;
    margin: 8px 0;
    border-bottom: 1px solid #4caf50;
    input{
      border: none;
      outline: none;
      background: none;
      color: white;
      font-size: 18px;
      margin: 0 10px;
      width: 80%;
      float: left;
      padding: 5px;
    }
    i{
      text-align: center;
      float: left;
      width: 26px;
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

