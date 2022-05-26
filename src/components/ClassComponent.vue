<template>
<div class="ClassComponent">
  <div class="c1 package">
    样式分离
  </div>
  <div :class="{ current: active }">
    实现样式的动态计算
  </div>
  <div :class="[current]">
    :class 可以使用数组的形式管理多个class样式
  </div>
  <div :class="[{ current: active }]">
    :class 也可以是数组对象的形式
  </div>
  <div :class="classLists">
   可以使用返回的数据
  </div>
</div>
</template>

<script>
  export default {
    data(){
      return{
        active:true,
        classLists:{
          current: true
        }
      }
    }
    
  }
</script>

<style lang="scss" scoped>

// scoped 使用css属性选择器的方法定义样式 可以有效地将组件像是隔离  会出现性能的开销
.ClassComponent{
  .c1 {
  color: white;
  }
  .current {
    background-color:#000;
    color: white;
  }
  // 为样式添加父级也可有效的隔离class样式




}
</style>