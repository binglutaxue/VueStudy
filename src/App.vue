<template>
<!-- <ClassComponent/> -->
<!-- <class-component/> -->
<!-- <ClassListComponent/> -->
<!-- <if-comment></if-comment> -->
<lesson-for></lesson-for>
<!-- <VForCommentVue/> -->
</template>

<script>
import ClassComponent from './components/ClassComponent.vue'
import ClassListComponent from "./components/ClassListComponent.vue"
import IfComment from './components/IfComment.vue'
import VForCommentVue from './components/VForComment.vue'
import LessonFor from './components/LessonFor.vue'
  export default {
    components: { ClassComponent ,ClassListComponent, IfComment,VForCommentVue,LessonFor},
    
  }
</script>

<style lang="scss" scoped>

</style>