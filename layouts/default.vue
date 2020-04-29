<template>
  <div class="flex flex-col h-screen">
    <logo-header />
    <div class="content border-dashed border-2">
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

<style>
.btn {
  @apply p-2 border border-solid border-gray-400 bg-black text-white;
}

.btn:hover {
  @apply bg-white text-black;
}

.content{
  border-color: crimson;
  flex: 1 0 auto;
}

.main-nav{
  flex-shrink: 0;
}
</style>
