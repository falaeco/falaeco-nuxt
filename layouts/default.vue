<template>
  <div class="flex flex-col h-screen">
    <logo-header />
    <div class="content border-dashed border-2">
      <nuxt />
    </div>
    <main-nav class="main-nav"/>
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

<style>
.content{
  border-color: crimson;
  flex: 1 0 auto;
}

.main-nav{
  flex-shrink: 0;
}
</style>
