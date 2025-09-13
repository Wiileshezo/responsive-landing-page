<script>
export default {};
</script>

<template>
  <section class="search-container">
    <h1>Search Courses</h1>
    <div class="search-box">
      <i class="fa-solid fa-magnifying-glass"></i>
      <input type="search" placeholder="Search for over 50+ courses" />
      <base-button mode="with-bg">Search</base-button>
    </div>
  </section>
  <section class="benefits">
    <div class="img-container">
      <div>
        <img src="../../images/1-g.png" alt="" class="img-g1 pink" />
        <img src="../../images/1-b.png" alt="" class="img-b1 purple" />
      </div>
      <div>
        <img src="../../images/2-g.png" alt="" class="img-g2 purple" />
        <img src="../../images/2-b.png" alt="" class="img-b2 pink" />
      </div>
    </div>
    <div class="benefits-container">
      <h1><i class="bold">Benefits</i> From Our Online Learning</h1>
      <div class="benefits-detials">
        <img src="../../images/graduate.png" alt="" class="purple icon" />
        <div>
          <h3>Online Degrees</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean
            commodo ligula eget dolor. Aenean massa.
          </p>
        </div>
      </div>
      <div class="benefits-detials">
        <img src="../../images/book.png" alt="" class="pink icon" />
        <div>
          <h3>Shorts Courses</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean
            commodo ligula eget dolor. Aenean massa.
          </p>
        </div>
      </div>
      <div class="benefits-detials">
        <img src="../../images/user.png" alt="" class="purple icon" />
        <div>
          <h3>Training From Experts</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean
            commodo ligula eget dolor. Aenean massa.
          </p>
        </div>
      </div>
      <div class="benefits-detials">
        <img src="../../images/play.png" alt="" class="pink icon" />
        <div>
          <h3>1.5k+ Video Courses</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean
            commodo ligula eget dolor. Aenean massa.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  background-color: var(--LightGrey);
}
h1 {
  text-align: center;
  font-weight: 600;
  font-size: 1.5rem;
  margin-block: 3rem 1rem;
}
.bold {
  font-weight: 700;
}
.search-container {
  display: flex;
  justify-content: center;
  flex-direction: column;
}
.search-box {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1rem;
}
i {
  color: var(--IconsBasePurple);
}
input {
  width: 40vw;
  border: none;
  background-color: #fff;
  border-radius: 1rem;
  padding: 0.5rem;
}

.benefits {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  padding: 1rem min(6rem, 10vw);
  gap: 5rem;
}
.img-container {
  display: flex;
  border: 0.2rem dashed var(--IconsBasePurple);
  border-radius: 5rem;
  padding: 0.3rem;
}
.img-container div {
  display: flex;
  flex-direction: column;
}
img {
  width: 10rem;
}
.img-g1 {
  border-radius: calc(5rem - 7px) 0;
}
.img-b1 {
  border-radius: 0 calc(5rem - 7px);
}
.img-g2 {
  border-radius: 0 calc(5rem - 7px);
}
.img-b2 {
  border-radius: calc(5rem - 7px) 0;
}

.purple {
  background-color: var(--IconsBasePurple);
}
.pink {
  background-color: var(--ButtonPink);
}

.benefits-container {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
.benefits-detials {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
}
h3 {
  font-weight: 700;
}
.icon {
  border-radius: 10px;
  width: 1rem;
  padding: 0.5rem;
}
@media (min-width: 800px) {
  .benefits {
    flex-direction: row;
  }
}
</style>
