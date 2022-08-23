<template>
  <div>
    <header>
      <ul>
        <li class="active">综合</li>
        <li>后端</li>
        <li>前端</li>
        <li>Android</li>
        <li>ios</li>
        <li>人工智能</li>
        <li>开发工具</li>
        <li>代码人生</li>
        <li>阅读</li>
      </ul>
    </header>
  </div>
</template>

<script>
export default {}
</script>

<style lang="less" scoped>
header {
  background-color: #fff;
  border-bottom: 1px solid #f1f1f1;
  width: 100%;
  height: 46px;
  ul {
    font-size: 14px;
    display: flex;
    align-items: center;
    line-height: 46px;
    color: gray;
    li:nth-child(1) {
      margin-left: 370px;
    }
    li {
      margin-right: 25px;
      cursor: pointer;
      &.active {
        color: #1e80ff;
      }
    }
    li:hover {
      color: #1e80ff;
    }
  }
}
</style>
