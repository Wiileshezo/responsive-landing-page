<script>
export default {};
</script>

<template>
  <section>
    <div class="instructor">
      <h1 class="title">
        If You Are A Certified Teacher Then
        <i class="purple">Become An Instructor</i>
      </h1>
      <p class="details">
        Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo
        ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis
        dis.
      </p>
      <h1 class="title margin-top">Enjoy Many Perks</h1>
      <div class="list-container">
        <ul class="list">
          <li>Lorem ipsum dolor sit amet.</li>
          <li>Consectetuer adipiscing elit.</li>
          <li>Aenean commodo ligula dolor.</li>
          <li>Penatibus et magnis dis.</li>
        </ul>
        <ul class="list">
          <li>Aenean massa.</li>
          <li>Cum sociis natoque penatibus.</li>
          <li>Penatibus et magnis dis.</li>
          <li>Consectetuer adipiscing elit.</li>
        </ul>
      </div>
      <base-button mode="with-bg">Become An Instructor </base-button>
    </div>
    <div class="instructor-img">
      <img src="@/images/instructor.png" alt="" />
    </div>
  </section>
</template>
<style scoped>
section {
  display: flex;
  flex-direction: column;
  padding: 4rem;
  align-items: center;
  justify-content: center;
  gap: 1rem;
}

.instructor {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 1rem;
}
.title {
  font-weight: 700;
  font-size: 1.6rem;
  max-width: 55vh;
}
.purple {
  font-weight: 700;
  color: var(--LinkTextPurple);
}
.details {
  font-size: calc(0.7rem + 0.3vw);
  max-width: 60ch;
}
.margin-top {
  margin-top: 1rem;
}
.list-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  gap: 1rem;
}
.list {
  padding-left: 2rem;
}
.list li {
  font-size: 0.8rem;
}
ul li::marker {
  list-style-type: disc;
  color: var(--LinkTextPurple);
  line-height: 2rem;
  font-size: 1.3rem;
}

.instructor-img {
  border-radius: 0 0 30vw 30vw;
  border: 2px dashed var(--ButtonPink);
  padding: 0.3rem;
}
img {
  width: 50vw;
  background: var(--ButtonPinkLG);
  border-radius: 0rem 0rem calc(30vw - 10px) calc(30vw - 10px);
}

@media (min-width: 500px) {
  section {
    flex-direction: row;
  }
  img {
    width: 30vw;
  }
}
</style>
