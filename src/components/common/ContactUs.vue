<script>
export default {};
</script>

<template>
  <section>
    <base-card class="card-style">
      <h1 class="header">Get In Touch</h1>
      <p class="details">
        Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo
        ligula eget dolor. Aenean massa.
      </p>
      <div>
        <input type="text" placeholder="Enter your email..." />
        <base-button class="bold">Subscribe</base-button>
      </div>
    </base-card>
  </section>
</template>

<style scoped>
section {
  display: flex;
  flex-direction: column;
  padding: calc(1rem + 10vw);
  background-color: var(--LightGrey);
  border-radius: 8rem 0;
}
.card-style {
  background: var(--ButtonPinkLG);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  padding: 3rem 2rem;
}
.header {
  color: var(--LightGrey);
  font-weight: 600;
  font-size: 1.5rem;
}
.details {
  color: var(--LightGrey);
  text-align: center;
  font-size: calc(0.7rem + 0.3vw);
  max-width: 60ch;
  margin: auto;
}
input {
  border: none;
  padding: 0.4rem;
  border-radius: 0.5rem;
  width: 25vw;
  color: var(--LightGrey);
}
.bold {
  font-weight: 500;
}
</style>
