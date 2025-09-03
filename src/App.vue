<script>
import TheNavigation from "./components/layouts/TheNavigation.vue";
import TheFooter from "./components/layouts/TheFooter.vue";
import HeroSection from "./components/common/HeroSection.vue";

export default {
  components: {
    TheNavigation,
    TheFooter,
    HeroSection,
  },
};
</script>

<template>
  <the-navigation></the-navigation>
  <hero-section></hero-section>
  <the-footer></the-footer>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Viga&display=swap");
:root {
  /* Primary Gradient Colors */
  --BrightPink: #ff5cf7;
  --PurpleGradientStart: #a362ff;
  --LightPurpleGradientEnd: #e1bbff;

  /*  Secondary & UI Colors*/
  --LightBackgroundWhite: #fdf9ff;
  --LightGrey: #f3f3f3; /* (Search/Input BG) */
  --DarkText: #2c2c2c; /* (Main headings) */
  --LightText: #777777; /*(Paragraphs) */
  --ButtonPink: #ff5da6; /*(Free Trial button) */
  --ButtonPinkLG: linear-gradient(
    to bottom,
    #c076ff,
    #ff5da6
  ); /*(Free Trial button) */
  --LinkTextPurple: #b66dff;

  /* Extra UI Elements */
  --ButtonHoverPurple: #8849df;
  --CourseCardShadowGrey: #dadada; /*(light drop shadow)*/
  --IconsBasePurple: #bc72ff;
  --FooterPurpleGradient: linear-gradient(to right, #c076ff, #913fff);
}
* {
  box-sizing: content-box;
  padding: 0;
  margin: 0;
  color: var(--DarkText);
  font-family: "Poppins", sans-serif;
  font-weight: 300;
  font-style: normal;
}
.poppins-bold {
  font-family: "Poppins", sans-serif;
  font-weight: 700;
  font-style: normal;
}
</style>
