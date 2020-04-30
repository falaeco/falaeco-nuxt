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
  @apply border border-solid border-gray-400 bg-gray-900 text-white;
}

.btn {
  @apply p-2 btn-colour-theme transition duration-150 ease-out;
}

.btn:hover {
  @apply bg-white text-black;
}
</style>
