<template>
  <div v-for="(lesson,index) in lessons" :key="index">
   <div v-if="lesson.isDelete" style="color:red">
   {{lesson.title}}
   </div>
   <div v-else-if="lesson.price>100" style="color:green">
    {{lesson.title}}
   </div>
   <div v-else>{{lesson.title}}</div>
   <div v-show="lesson.isDelete">{{ lesson.title}}</div> 
   <!-- v-if 不会生成div v-show会生成div只是隐藏 -->
  </div>
</template>

<script>
import lessons from "../../data/lessons"
  export default {
    data(){
      return {
        lessons
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>