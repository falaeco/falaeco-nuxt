<template>
  <div class="p-container border border-solid border-blue-500 flex flex-col md:flex-row">
    <project-nav />
    <div class="h-full">
      <nuxt-child />
    </div>
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
.p-container {
  height: 100%;
}
</style>
