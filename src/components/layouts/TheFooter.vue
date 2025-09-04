<script></script>

<template>
  <section>
    <base-card>
      <img src="../../images/iileshzo-removebg.png" alt="" />
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, <br />sed do
        eiusmod tempor incididunt.
      </p>
      <i class="fa-brands fa-facebook"></i>
      <i class="fa-brands fa-x-twitter"></i>
      <i class="fa-brands fa-telegram"></i>
    </base-card>
    <base-card>
      <h2>Company</h2>
      <ul>
        <li>About Us</li>
        <li>Services</li>
        <li>Community</li>
        <li>Testimonials</li>
      </ul>
    </base-card>
    <base-card>
      <h2>Support</h2>
      <ul>
        <li>Help Center</li>
        <li>Tweet @ Us</li>
        <li>Webinars</li>
        <li>Feedback</li>
      </ul>
    </base-card>
    <base-card>
      <h2>Links</h2>
      <ul>
        <li>Courses</li>
        <li>Become Teacher</li>
        <li>service</li>
        <li>All in One</li>
      </ul>
    </base-card>
    <base-card>
      <h2>Contact Us</h2>
      <ul>
        <li>+(000) 123-4567</li>
        <li>example@eimail.com</li>
      </ul>
    </base-card>
  </section>
</template>

<style scoped>
section {
  background: var(--ButtonPinkLG);
  display: flex;
  justify-content: center;
}
img {
  width: 4rem;
}

i,
h2 {
  color: var(--LightGrey);
  font-size: 1rem;
}
ul {
  list-style: none;
}
p,
li {
  color: var(--LightGrey);
  font-size: 0.7rem;
}
</style>
