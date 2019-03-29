<template>
  <div class="middle search-box">
    <input class="search-txt" type="text" name placeholder="搜索">
    <a href="#" class="search-btn iconfont icon-search"></a>
  </div>
</template>

<script>
export default {
  name: "SearchButton",
  data() {
    return {};
  }
};
</script>

<style scoped lang="scss">
.search-box {
  background: #2f3640;
  height: 40px;
  border-radius: 40px;
  padding: 10px;
  &:hover > .search-txt {
    width: 240px;
    padding: 0 6px;
  }
  &:hover > .search-btn {
    background: white;
  }
  .search-txt {
    border: none;
    background: none;
    outline: none;
    float: left;
    padding: 0;
    color: white;
    font-size: 16px;
    transition: 0.4s;
    line-height: 40px;
    width: 0px;
  }
  .search-btn {
    text-decoration: none;
    color: #e74c3c;
    float: right;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background: #2f3640;
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>
