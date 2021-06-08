<template>
  <button :class="dark ? 'darkBtn' : ''">Schedule a visit</button>
</template>

<script>
export default {
  props: {
    dark: Boolean,
  },
}
</script>

<style lang="scss" scoped>
button {
  padding: 16px 46px;
  border-radius: 50px;
  font-weight: 100;
  box-shadow: none;
  border: none;
}

.darkBtn{
    background:#545871;
    color:white;
}
</style>