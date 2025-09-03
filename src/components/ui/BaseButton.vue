<script>
export default {
  props: ["type", "mode"],
};
</script>

<template>
  <button :type="type" :class="mode">
    <slot></slot>
  </button>
</template>

<style scoped>
button {
  padding: 0.2rem 1rem;
  border-radius: 0.5rem;
  border: solid 1px var(--ButtonPink);
  margin-inline: 0.3rem;
}
.with-bg {
  background: var(--ButtonPinkLG);
  color: var(--LightGrey);
  border: none;
}
.with-bg:hover,
.with-bg:active {
  background: var(--LightGrey);
  color: var(--ButtonPink);
  border: solid 1px var(--ButtonPink);
}
</style>
