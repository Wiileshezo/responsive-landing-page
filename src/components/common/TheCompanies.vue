<script>
export default {};
</script>

<template>
  <section>
    <img src="@/images/Duolingo.png" alt="" />
    <img src="@/images/magic-leap.png" alt="" />
    <img src="@/images/microsoft.png" alt="" />
    <img src="@/images/codecov.png" alt="" />
    <img src="@/images/user-testing.png" alt="" />
  </section>
</template>

<style scoped>
section {
  background: var(--ButtonPinkLG);
  /* background: var(--FooterPurpleGradient); */
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-evenly;
  align-items: center;
  padding: 1rem;
  row-gap: 1rem;
}
img {
  width: 4.3rem;
}

@media (min-width: 700px) {
  img {
    width: 6rem;
  }
}
</style>
