<template>
  <div class="h-screen">
    <logo-header />
    <div class="content">
      <nuxt />
    </div>
    <main-nav class="main-nav" />
  </div>
</template>

<script>
import LogoHeader from '@/components/LogoHeader'
import MainNav from '@/components/MainNav'
export default {
  components: {
    LogoHeader, MainNav
  }
}
</script>

<style scoped>
/** the content needs to be height - topBar - bottomBar */
@media screen and (min-width: 768px){
  .content {
    height: calc(100% - 80px);
  }
}
</style>
