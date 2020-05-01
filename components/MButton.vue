<template>
  <button class="btn">
    <slot />
  </button>
</template>

<script>
export default {
  name: 'MButton'
}
</script>

<style lang="postcss">
.btn-colour-theme{
  @apply bg-mdarktwo text-mwhite;
}

.btn {
  @apply p-2 btn-colour-theme transition duration-150 ease-out;
}

.btn:hover {
  @apply bg-mwhite text-mdarktwo;
}
</style>
