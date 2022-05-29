<template>
  <div>
            <!-- vue-for
             -->
             <!-- v-for 数值 循环-->
             <div v-for=" n in 8" :key="n">
             {{ n }}
             </div>

             <!-- v-for 循环对象 -->
             <div v-for="(value,key,index) in obj"  :key="index">
              {{ key }}----{{ value }}
             </div>
             <!-- v-for 和 v-if 不能在同一个容器中使用 -->
  </div>
</template>

<script>
  export default {
    data(){
      return {
         obj:{
          name: "java",
          url:"javahtt"
       }
      }
    }
    
  }
</script>

<style lang="scss" scoped>

</style>