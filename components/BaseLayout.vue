<template>
  <div class="layout" :style="{ padding }">
    <div class="layout__container" :class="[columns, center ? 'center' : '']">
      <slot />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    padding: {
      type: String,
      default: '4rem',
    },
    center: Boolean,
    columns: {
      type: String,
      default: 'one',
    },
  },
}
</script>

<style lang="scss" scoped>
$mainwidth: 1400px;
$gap: 50px;
.layout {
  width: $mainwidth;
  max-width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: auto;

  height: 100%;
  &__container {
    display: grid;
    gap: $gap;
    align-items: center;
  }
  .center {
    text-align: center;
    justify-content: center;
  }
  .one {
    grid-template-columns: 1fr;
  }
  .two {
    grid-template-columns: repeat(
      auto-fit,
      minmax(($mainwidth/2)-$gap * 3, 1fr)
    );
  }
  .three {
    grid-template-columns: repeat(
      auto-fit,
      minmax(($mainwidth/3)-$gap * 3, 1fr)
    );
  }
}
</style>