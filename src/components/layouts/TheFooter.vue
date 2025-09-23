<script></script>

<template>
  <section>
    <div class="boxes">
      <img src="@/images/iileshzo-removebg.png" alt="" />
      <p>
        Lorem ipsum dolor sit amet,<br />
        consectetur adipiscing elit, <br />sed do eiusmod tempor incididunt.
      </p>
      <i class="fa-brands fa-facebook"></i>
      <i class="fa-brands fa-x-twitter"></i>
      <i class="fa-brands fa-telegram"></i>
    </div>
    <div class="boxes">
      <h1>Company</h1>
      <ul>
        <li>About Us</li>
        <li>Services</li>
        <li>Community</li>
        <li>Testimonials</li>
      </ul>
    </div>
    <div class="boxes">
      <h1>Support</h1>
      <ul>
        <li>Help Center</li>
        <li>Tweet @ Us</li>
        <li>Webinars</li>
        <li>Feedback</li>
      </ul>
    </div>
    <div class="boxes">
      <h1>Links</h1>
      <ul>
        <li>Courses</li>
        <li>Become Teacher</li>
        <li>service</li>
        <li>All in One</li>
      </ul>
    </div>
    <div class="boxes">
      <h1>Contact Us</h1>
      <ul>
        <li>+(000) 123-4567</li>
        <li>example@eimail.com</li>
      </ul>
    </div>
    <div class="attribution">
      <hr />
      <a href="https://github.com/Wiileshezo">
        Copyright <i class="fa-solid fa-copyright"></i> 2025 Wiileshezo . All
        rights reserved</a
      >.
    </div>
  </section>
</template>

<style scoped>
section {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: space-between;
  padding: 4rem;
}
.boxes {
  padding: 0.5rem;
  width: 15vw;
}
img {
  width: 4rem;
}

i,
h1 {
  color: var(--LightGrey);
  font-size: 1.2rem;
  padding-bottom: 1rem;
}
h1 {
  font-weight: 700;
}
ul {
  list-style: none;
}
li {
  line-height: 2rem;
}
p,
li {
  color: var(--LightGrey);
  font-size: 0.8rem;
}
.attribution {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: auto;
}
.attribution > a {
  color: var(--LightGrey);
  font-size: 10px;
  margin-top: 1rem;
  text-decoration-line: none;
}
.attribution i {
  color: var(--LightGrey);
  font-size: 0.7rem;
}
hr {
  border: none;
  width: 65vw;
  height: 2px;
  display: block;
  background: radial-gradient(
    ellipse at center,
    var(--LightGrey) 0%,
    var(--LightGrey) 30%,
    transparent 100%
  );
}

@media (max-width: 800px) {
  .boxes {
    width: 15vw;
  }
}
@media (max-width: 770px) {
  .boxes {
    width: 38vw;
  }
}
@media (max-width: 450px) {
  .boxes {
    width: 100vw;
  }
}
</style>
