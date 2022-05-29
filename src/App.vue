<template>
<!-- <ClassComponent/> -->
<!-- <class-component/> -->
<!-- <ClassListComponent/> -->
<if-comment></if-comment>
<VForCommentVue/>
</template>

<script>
import ClassComponent from './components/ClassComponent.vue'
import ClassListComponent from "./components/ClassListComponent.vue"
import IfComment from './components/IfComment.vue'
import VForCommentVue from './components/VForComment.vue'
  export default {
    components: { ClassComponent ,ClassListComponent, IfComment,VForCommentVue},
    
  }
</script>

<style lang="scss" scoped>

</style>