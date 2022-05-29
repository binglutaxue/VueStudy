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