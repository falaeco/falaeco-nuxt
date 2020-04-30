<template>
  <div>
    <nav class="project-nav py-4">
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
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.project-nav{
  border: 2px dashed darkblue;
}

.nuxt-link-active {
  border-bottom: 2px solid black;
}
</style>
