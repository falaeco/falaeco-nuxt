<template>
  <nav class="text-center p-8">
    <nuxt-link to="/projects">
      Projects
    </nuxt-link>
    <span class="mx-2">//</span>
    <nuxt-link to="/about">
      About
    </nuxt-link>
  </nav>
</template>

<script>
export default {

}
</script>

<style scoped>
.nuxt-link-active{
 border-bottom: 2px solid black
}
</style>
