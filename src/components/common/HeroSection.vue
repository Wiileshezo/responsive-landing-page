<script></script>

<template>
  <section>
    <div class="p-side">
      <h1>Develop your skills in a new and unique way</h1>
      <p>
        Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo
        ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis
      </p>
      <div>
        <base-button mode="with-bg">Enroll Now</base-button>
        <base-button>About Us</base-button>
      </div>
    </div>
    <div class="img-side">
      <img src="../../images/lg.png" alt="" />
      <div class="badge-container badge-1">
        <div>
          <span class="plus-icon">
            <i class="fa-solid fa-arrow-up arrow"></i>
          </span>
        </div>
        <div>
          <span class="badge-number"> 50+ </span>
          <span class="details"> Online Courses </span>
        </div>
      </div>

      <div class="badge-container badge-2">
        <span class="badge-number">10k+</span>
        <span class="details">Online Students</span>
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  margin-top: 5rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-inline: 3rem;
  background: var(--LightBackgroundWhite);
}
.p-side {
  width: 80vw;
  text-align: center;
}
.p-side p {
  font-size: calc(0.7rem + 0.3vw);
}
.p-side div {
  margin-block: 1rem;
}
h1 {
  font-weight: 700;
}
.img-side {
  width: 100vw;
  display: flex;
  justify-content: center;
  position: relative;
}
img {
  width: 80vw;
}

.badge-container {
  display: flex;
  align-items: center;
  background-color: rgb(255 255 255 / 81%);
  padding: 0.3rem 0.5rem;
  border-radius: 0.8rem;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  color: #333;
}
.badge-1 {
  flex-direction: row;
  position: absolute;
  gap: 0.5rem;
  left: 2%;
  top: 30%;
}
.badge-2 {
  flex-direction: column;
  position: absolute;
  right: 2%;
  top: 65%;
}

.badge-container div {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.badge-number {
  display: flex;
  align-items: center;
  gap: 5px;
  font-weight: bold;
  color: var(--PurpleGradientStart);
  font-size: 0.7rem;
}
.plus-icon {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 20px;
  height: 20px;
  background-color: var(--PurpleGradientStart);
  color: white;
  border-radius: 1rem;
  font-size: 0.7rem;
  font-weight: bold;
}
.arrow {
  transform: rotate(-40deg);
  color: var(--LightGrey);
  font-size: 0.5rem;
}
.details {
  font-size: 0.7rem;
  color: #333;
}

@media (min-width: 500px) {
  section {
    flex-direction: row;
    margin-top: 3rem;
  }
  .p-side {
    width: 60vw;
    text-align: left;
  }
  .img-side {
    width: 40vw;
  }
  img {
    width: 40vw;
  }
}
</style>
