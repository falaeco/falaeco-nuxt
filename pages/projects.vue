<template>
  <div class="project-view-container h-full flex flex-col">
    <project-nav />
    <nuxt-child class="h-full" />
  </div>
</template>

<script>
import ProjectNav from '@/components/ProjectNav'

export default {
  components: {
    ProjectNav
  }
}
</script>

<style scoped>
.project-view-container{
  border: 1px solid brown;
}
</style>
