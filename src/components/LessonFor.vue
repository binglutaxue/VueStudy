<template>
  <div>
    <!-- 11123 -->

    <button @click=" orderBy = 'price'">价格排序</button>
    <button @click=" orderBy = 'comments'">评论数排序</button>

    <!-- {{orderBy}} -->
    <!-- 升序降序 -->
    
    <button @click="lessonLists = 'asc'"> 升序</button>
    <button @click="lessonLists = 'desc'">降序</button>

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
        orderBy: 'price',
        // 默认价格排序
        orderType: 'asc'
      }
    },
    computed: { 

       lessonLists: {
        //  console.log(this.lessons);
        //  console.log(this.lessons);
         get(){
            return this.lessons.sort((a,b)=>{
             return this.orderType == 'asc'? a[this.orderBy] - b[this.orderBy]:b[this.orderBy]-a[this.orderBy]

          })
         },
         set(type) {
            this.orderType = type
         }
       }
    }
  }
</script>

<style lang="scss" scoped>

</style>