<template>
  <nav>
    <nuxt-link :to="{name: 'projects-equilibria'}">
      Equilibria
    </nuxt-link>
    <nuxt-link :to="{name: 'projects-machineforbirds'}">
      Machine For Birds
    </nuxt-link>
    <nuxt-link :to="{name: 'projects-ruinism'}">
      Ruinism
    </nuxt-link>
  </nav>
</template>

<script>
export default {

}
</script>

<style scoped>

.nuxt-link-active {
  border-bottom: 2px solid black;
}
</style>
