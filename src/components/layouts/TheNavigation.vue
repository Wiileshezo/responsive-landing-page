<script></script>

<template>
  <header>
    <a href="#">
      <img src="@/images/wiileshzo-removebg.png" alt="logo" class="nav-logo" />
    </a>
    <input type="checkbox" id="check" />
    <label for="check" class="icon-label">
      <i class="fa-solid fa-bars icon" id="menu"></i>
      <i class="fa-solid fa-close icon" id="close"></i>
    </label>
    <nav>
      <ul>
        <li style="--i: 0"><a href="">Home</a></li>
        <li style="--i: 1"><a href="">Courses</a></li>
        <li style="--i: 2"><a href="">Teachers</a></li>
        <li style="--i: 3"><a href="">Contact</a></li>
      </ul>
      <div>
        <base-button style="--j: 0">Sign in</base-button>
        <base-button style="--j: 1" mode="with-bg">Free Trial</base-button>
      </div>
    </nav>
  </header>
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-around;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: var(--LightBackgroundWhite);
  z-index: 100;
}

nav {
  display: flex;
  align-items: center;
}
ul {
  list-style: none;
  display: flex;
}
li > a {
  text-decoration-line: none;
  font-weight: 500;
  padding-inline: 0.5rem;
}
.nav-logo {
  width: 3rem;
}
div > button {
  display: inline;
  margin: 0.3rem;
}
.icon-label {
  position: absolute;
  cursor: pointer;
  display: none;
  right: 5%;
}
.icon {
  color: var(--ButtonPink);
  font-size: 1.3rem;
}
#check {
  display: none;
}

/* media */
@media (max-width: 900px) {
  nav {
    display: block;
  }
  ul {
    display: block;
  }
  div > button {
    display: block;
  }
}
@media (max-width: 870px) {
  header {
    justify-content: flex-start;
  }
  .nav-logo {
    padding-inline-start: 3rem;
  }
  nav {
    position: absolute;
    width: 100%;
    top: 100%;
    left: 0;
    height: 0;
    background-color: var(--ButtonPink);
    align-content: center;
    overflow: hidden;
    transition: 0.3s ease;
    text-align: center;
  }
  #check:checked ~ nav {
    height: 17rem;
  }

  nav ul li {
    font-size: 1.1rem;
    transform: translateY(-50px);
    transition: 0.3s ease;
    line-height: 2rem;
  }
  #check:checked ~ nav ul li {
    transform: translateY(0);
    transition: calc(0.2s * var(--i));
    opacity: 1;
  }

  div {
    display: inline-block;
  }
  div button {
    margin-inline: auto;
    margin-block: 0.5rem;
    transform: translateY(10px);
    transition: 0.3s ease-in;
  }
  #check:checked ~ div button {
    transform: translateY(0);
    transition: calc(0.2s * var(--j));
  }
  .icon-label {
    display: block;
  }
  #check:checked ~ .icon-label #menu {
    display: none;
  }
  #check:checked ~ .icon-label #close {
    display: block;
  }
  #close {
    display: none;
  }
}
</style>
