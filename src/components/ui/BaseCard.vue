<script>
export default {};
</script>

<template>
  <div class="card" :type="type" :class="mode">
    <slot></slot>
  </div>
</template>

<style scoped>
.card {
  border-radius: 2rem;
  background-color: var(--LightBackgroundWhite);
}
</style>
