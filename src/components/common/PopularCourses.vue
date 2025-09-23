<script>
import c1 from "@/images/c1.jpeg";
import c2 from "@/images/c2.jpeg";
import c3 from "@/images/c3.jpeg";
import JS from "@/images/jungsuk.jpg";
import WB from "@/images/woobin.jpg";
import SH from "@/images/shinhye.jpg";
export default {
  data() {
    return {
      courses: [
        {
          img: c1,
          type: "Web Design",
          rate: 4.5,
          title: "Web Design & Development",
          classes: "25 Classes",
          students: "185 Students",
          price: 560.0,
          teacher: "Lee Jong Suk",
          tImg: JS,
        },
        {
          img: c2,
          type: "UI/UX Design",
          rate: 4.3,
          title: "Wierframing prototyping",
          classes: "8 Classes",
          students: "400 Students",
          price: 600.0,
          teacher: "Kim Woo Bin",
          tImg: WB,
        },
        {
          img: c3,
          type: "Data Science",
          rate: 4.7,
          title: "Python For Data Science",
          classes: "17 Classes",
          students: "100 Students",
          price: 490.0,
          teacher: "Park Shin Hye",
          tImg: SH,
        },
      ],
    };
  },
};
</script>

<template>
  <section class="courses-container">
    <h1 class="header">Our Popular Courses</h1>
    <p class="details">
      Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo
      ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis
      dis.
    </p>
    <div class="cards-container">
      <base-card v-for="(course, index) in courses" :key="index" class="card">
        <img :src="course.img" :alt="course.title" class="img" />
        <div class="df">
          <p class="type df">
            <i class="fa-solid fa-circle circle"></i> {{ course.type }}
          </p>
          <p class="rate df">
            <i class="fa-solid fa-star star"></i> {{ course.rate }}
          </p>
        </div>
        <h2 class="title">{{ course.title }}</h2>
        <div class="df">
          <p class="classes">
            <i class="fa-solid fa-book-open purple-font"></i>
            {{ course.classes }}
          </p>
          <p class="students">
            <i class="fa-regular fa-user purple-font"></i>
            {{ course.students }}
          </p>
        </div>
        <hr class="light-purple" />
        <div class="df">
          <p class="price">${{ course.price }}</p>

          <p class="teacher purple-font df">
            <img :src="course.tImg" alt="" class="t-img" /> {{ course.teacher }}
          </p>
        </div>
      </base-card>
    </div>
  </section>
</template>

<style scoped>
.courses-container {
  background: var(--ButtonPinkLG);
  text-align: center;
  padding-block: 3rem;
  display: flex;
  flex-direction: column;
  gap: 2rem;
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
.cards-container {
  display: flex;
  gap: 2rem;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
.card {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  padding: 0.6rem 0.6rem 1.3rem 0.6rem;
}
.df {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 0.5rem;
}
.img {
  width: 23vw;
  border-radius: calc(2rem - 10px);
  margin: auto;
}
.type {
  background-color: var(--LightPurple);
  color: var(--ButtonHoverPurple);
  padding: 0.2rem 0.5rem;
  border-radius: 0.5rem;
  font-size: 0.8rem;
}
.circle {
  color: var(--ButtonHoverPurple);
  font-size: 0.5rem;
}
.star {
  color: yellow;
  font-size: 0.4rem;
}
.rate {
  background-color: var(--ButtonHoverPurple);
  color: var(--LightGrey);
  padding: 0.2rem 0.5rem;
  border-radius: 0.5rem;
  font-size: 0.8rem;
}
.title {
  font-size: 1rem;
  font-weight: 600;
  padding-block: 0.5rem;
  text-align: left;
}
.light-purple {
  background-color: var(--LightPurple);
}
.purple-font {
  color: var(--ButtonHoverPurple);
}
.classes,
.students,
.teacher {
  font-size: 0.8rem;
  font-weight: 500;
}
hr {
  border: none;
  height: 2px;
  background: radial-gradient(
    ellipse at center,
    var(--LightPurple) 0%,
    var(--LightPurple) 30%,
    transparent 100%
  );
}
.price {
  font-size: 1rem;
  font-weight: 700;
}
.t-img {
  width: 2rem;
  border-radius: 50%;
}

@media (min-width: 500px) {
  .cards-container {
    flex-direction: row;
  }
}
@media (max-width: 770px) {
  .img {
    width: 26vw;
  }
}
@media (max-width: 500px) {
  .img {
    width: 63vw;
  }
}
</style>
