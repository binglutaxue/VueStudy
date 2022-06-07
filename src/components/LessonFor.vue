<template>
  <div>
    <!-- 11123 -->

    <button @click=" orderBy = 'price'">价格排序</button>
    <button @click=" orderBy = 'comments'">评论数排序</button>

    {{orderBy}}
    <template v-for="leson in lessonLists" :key="leson.id">
      <div>{{leson.title}}-价格:{{ leson.price }} - 评论数： {{ leson.comments }}</div>
    </template>
  </div>
</template>

<script>
import lessons from '../../data/lessons'
  export default {
    data(){
      return {
        lessons,
        orderBy: 'price'
        // 默认价格排序

      }
    },
    computed: { 
       lessonLists() {
        //  console.log(this.lessons);
        //  console.log(this.lessons);
          return this.lessons.sort((a,b)=>{
             return a[this.orderBy] - b[this.orderBy]

          })
       }
    }
  }
</script>

<style lang="scss" scoped>

</style>