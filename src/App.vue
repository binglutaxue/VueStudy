<template>
<ClassComponent/>
<!-- <class-component/> -->
<ClassListComponent/>
</template>

<script>
import ClassComponent from './components/ClassComponent.vue'
import ClassListComponent from "./components/ClassList.Component.vue"
  export default {
    components: { ClassComponent ,ClassListComponent},
    
  }
</script>

<style lang="scss" scoped>

</style>