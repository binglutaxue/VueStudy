<template>
<div class="ClassComponent">
  <div class="c1">
    样式分离
  </div>
</div>
</template>

<script>
  export default {
    
  }
</script>

<style lang="scss" scoped>

// scoped 使用css属性选择器的方法定义样式 可以有效地将组件像是隔离  会出现性能的开销
.ClassComponent{
  .c1 {
  color: red;
  }

  // 为样式添加父级也可有效的隔离class样式




}
</style>