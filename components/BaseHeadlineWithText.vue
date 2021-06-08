<template>
  <div class="textbox" :style="{ marginBottom }">
    <h2>{{ title }}</h2>
    <p>{{ text }}</p>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    text: String,
    marginBottom: String,
  },
}
</script>

<style lang="scss" scoped>
.textbox {
  max-width: 100%;
}
</style>