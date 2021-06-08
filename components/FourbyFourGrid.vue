<template>
  <div class="grid-4-4">
    <slot />
  </div>
</template>

<style scoped>
.grid-4-4 {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(256px, 1fr));
  grid-gap: 2rem;
  max-width: 100%;
}
</style>