<template>
  <nav class="content-nav flex flex-row justify-center md:flex-col">
    <nuxt-link :to="{name: 'projects-equilibria'}" class="content-link">
      Equilibria
    </nuxt-link>
    <nuxt-link :to="{name: 'projects-machineforbirds'}" class="content-link">
      Machine For Birds
    </nuxt-link>
    <nuxt-link :to="{name: 'projects-ruinism'}" class="content-link">
      Ruinism
    </nuxt-link>
  </nav>
</template>

<script>
export default {

}
</script>

<style scoped lang="postcss">
.content-nav {
  border-top: 1px solid;
  border-bottom: 1px solid;
  @apply border-mdarktwo;
}

.content-nav .content-link:not(:last-child){
  @apply mr-2;
}

.content-link {
  border-top: 2px solid transparent;
  padding: 0.25rem 0;
  padding-bottom: calc(0.25rem + 2px);
  text-transform: uppercase;
}

.nuxt-link-active {
  @apply border-mwhite;
  border-top: 2px solid;
}
</style>
