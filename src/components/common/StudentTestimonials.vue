<script setup>
import JS from "@/images/jungsuk.jpg";
import WB from "@/images/woobin.jpg";
import SH from "@/images/shinhye.jpg";
import HJ from "@/images/hyojoo.jpeg";

import { ref, onMounted } from "vue";

const students = [
  {
    img: WB,
    type: "Web Design",
    title: "Web Design & Development",
    description:
      "Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa.",
  },
  {
    img: SH,
    type: "UI/UX Design",
    title: "Wierframing prototyping",
    description:
      "Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa.",
  },
  {
    img: JS,
    type: "Data Science",
    title: "Python For Data Science",
    description:
      "Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa.",
  },
  {
    img: HJ,
    type: "UI/UX Design",
    title: "Wierframing prototyping",
    description:
      "Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa.",
  },
];

const slider = ref(null);
const currentIndex = ref(1);
const total = students.length;

// Update current index when scrolled
const updateIndex = () => {
  const slideWidth = slider.value.offsetWidth;
  const idx = Math.round(slider.value.scrollLeft / slideWidth) + 1;
  currentIndex.value = idx;
};

// Prev/Next navigation
const prev = () => {
  const slideWidth = slider.value.offsetWidth;
  slider.value.scrollBy({ left: -slideWidth, behavior: "smooth" });
};
const next = () => {
  const slideWidth = slider.value.offsetWidth;
  slider.value.scrollBy({ left: slideWidth, behavior: "smooth" });
};

onMounted(() => {
  slider.value.addEventListener("scroll", updateIndex);
});
</script>

<template>
  <section>
    <h1 class="header">Student's Testimonials</h1>
    <p class="details">
      Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo
      ligula eget dolor. Aenean massa.
    </p>
    <div class="slider">
      <!-- Slides -->
      <div class="slides" ref="slider">
        <div v-for="(student, index) in students" :key="index" class="slide">
          <base-card class="card">
            <div class="upper-card">
              <img :src="student.img" alt="{{ student.title }}" class="img" />
              <div>
                <h2 class="title">{{ student.title }}</h2>
                <p class="type">{{ student.type }}</p>
                <div>
                  <i class="fa-solid fa-star star yellow"></i>
                  <i class="fa-solid fa-star star yellow"></i>
                  <i class="fa-solid fa-star star yellow"></i>
                  <i class="fa-solid fa-star star yellow"></i>
                  <i class="fa-solid fa-star-half yellow"></i>
                </div>
              </div>
            </div>
            <p class="description">{{ student.description }}</p>
          </base-card>
        </div>
      </div>
      <!-- Controls -->
      <div class="controls">
        <button @click="prev" class="prev">‹</button>
        <span class="indicator">{{ currentIndex }} / {{ total }}</span>
        <button @click="next" class="next">›</button>
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
  gap: 2rem;
  padding-block: 3rem;
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

.card-container {
  display: flex;
  gap: 1rem;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding-inline: 3rem;
}
.card {
  padding: 1rem;
}
/* .card:hover {
  box-shadow: 0 10px 10px rgb(0 0 0 / 40%);
} */

.upper-card {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  text-align: left;
  gap: 1rem;
}
.img {
  width: 5rem;
  border-radius: 50%;
}
.title {
  font-size: 0.9rem;
  font-weight: 700;
}
.type {
  font-size: 0.7rem;
}
.yellow {
  color: yellow;
  font-size: 0.5rem;
}
.description {
  font-size: 0.8rem;
}

/* Container */
.slider {
  position: relative;
  overflow: hidden;
  width: 100%;
  max-width: 900px;
  margin: auto;
  min-height: max(35vh, 15rem);
}

/* Slides wrapper */
.slides {
  display: flex;
  scroll-snap-type: x mandatory;
  overflow-x: auto;
  scroll-behavior: smooth;
  scrollbar-width: none; /* hide scrollbar */
}
.slides::-webkit-scrollbar {
  display: none;
}

/* Slide */
.slide {
  flex: 0 0 100%;
  scroll-snap-align: start;
  height: 200px;
  display: flex;
  align-items: center;
  justify-content: center;

  margin: 0 0.5rem;
}

/* Responsive */
@media (min-width: 768px) {
  .slide {
    flex: 0 0 50%;
  }
}
@media (min-width: 1024px) {
  .slide {
    flex: 0 0 32%;
  }
}

/* Controls */
.controls {
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  align-items: flex-end;
  gap: 1rem;
}
.controls button {
  background: transparent;
  border: none;
  border-radius: 50%;
  width: 36px;
  height: 36px;
  font-size: 2rem;
  font-weight: 600;
  cursor: pointer;
  /* box-shadow: 0 2px 6px rgba(0, 0, 0, 0.2); */
  color: var(--LightGrey);
}
.controls .indicator {
  font-size: 1rem;
  color: var(--LightGrey);
}

@media (min-width: 500px) {
  .card-container {
    flex-direction: row;
  }
}
</style>
