<template>
  <div class="classlist">
    <div v-for="(list,index) in lessons" :key="index">
    <span :class="{'is-delete':list.isDelete}">{{ list.title }}</span>
    <button @click="list.isDelete = !list.isDelete">
      {{list.isDelete?'取消':'删除'}}
    </button>
  </div>
  </div>
</template>

<script>
import lessons from '../../data/lessons'
  export default {
    data(){
      return {
        lessons
      }
    } 
  }
</script>

<style lang="scss" scoped>
  .classlist{
    div{
       display:flex;
       justify-content: space-between;
       span {
         &.is-delete {
           text-decoration: line-through;
         }
       }
    }
  }
</style>