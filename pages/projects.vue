<template>
  <div class="project-view-container">
    <project-nav />
    <nuxt-child/>
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
