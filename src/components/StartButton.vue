<template>
  <div>
    <a href="#">Get Started</a>
  </div>
</template>

<script>
export default {
  name: "StartButton",
  data() {
    return {};
  }
};
</script>

<style scoped lang="scss">
a {
  text-decoration: none;
  color: white;
  background-color: rgba(52, 152, 219,1.0);
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  padding: 75px 30px;
  border-radius: 50%;
  font-size: 20px;
  text-transform: uppercase;
  font-family: sans-serif;
  animation: animate 2s infinite linear    ;

}

@keyframes animate {
  0%{
    box-shadow: 0 0 0 0 rgba(52, 152, 219,0.6);
  }  
  30%{
    box-shadow: 0 0 0 50px rgba(52, 152, 219,0);
  }  
  65%{
    box-shadow: 0 0 0 50px rgba(52, 152, 219,0);
  }  
  100%{
    box-shadow: 0 0 0 0 rgba(52, 152, 219,0);
  }  

}
</style>
