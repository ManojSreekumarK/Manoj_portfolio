<template>
  <section class="hero">
    <div>
      <h1>I am <span>Manoj Sreekumar</span> and I am a <span>front-end developer</span></h1>
      <p>
        Welcome to my portfolio! I'm a passionate frontend developer with a love for creating
        visually appealing and interactive web experiences.
      </p>
      <button style="--clr: #c778dd"><span>Contact me!!</span><i></i></button>
    </div>
    <div>
      <img src="src/assets/homepage/ManojSreekumar.png" />
      <container class="status"
        ><div class="purple-square"></div>
        <span>Currently working for Pitsolutions</span></container
      >
    </div>
  </section>
  <div class="Quote">
    <img src="@/assets/homepage/Quote.svg" />
    <h3>On the other side of the screen, it all looks so easy</h3>
    <img src="@/assets/homepage/Quote.svg" />
    <h3>-"Tron" (1982)</h3>
  </div>
</template>

<script setup lang="ts"></script>

<style lang="scss" scoped>
@import 'src/styles/varables';
.hero {
  display: flex;
  align-items: center;
  justify-content: center;
  max-width: $layout-col1;
  gap: 10px;
  margin: 62px auto;

  div:last-of-type {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 469px;
    height: calc(386px + 37px);
  }
  div:first-of-type {
    width: 537px;
    height: 227px;
  }
}
h1 span {
  color: $secondary-color;
}
p {
  margin: 32px 0 24px;
}
.status {
  display: block;
  width: 402px;
  height: 37px;
  background: #282c33;
  border: 1px solid #abb2bf;
}
///////
///
button {
  position: relative;
  background: #444;
  color: #fff;
  text-decoration: none;
  text-transform: uppercase;
  border: none;
  letter-spacing: 0.1rem;
  font-size: 1rem;
  padding: 0.8rem 2rem;
  transition: 0.2s;
}

button:hover {
  letter-spacing: 0.2rem;
  padding: 0.9rem 2.1rem;
  background: var(--clr);
  color: var(--clr);
  /* box-shadow: 0 0 35px var(--clr); */
  animation: box 3s infinite;
}

button::before {
  content: '';
  position: absolute;
  inset: 2px;
  background: #272822;
}

button span {
  position: relative;
  z-index: 1;
}
button i {
  position: absolute;
  inset: 0;
  display: block;
}

button i::before {
  content: '';
  position: absolute;
  width: 10px;
  height: 2px;
  left: 80%;
  top: -2px;
  border: 2px solid var(--clr);
  background: #272822;
  transition: 0.2s;
}

button:hover i::before {
  width: 15px;
  left: 20%;
  animation: move 3s infinite;
}

button i::after {
  content: '';
  position: absolute;
  width: 10px;
  height: 2px;
  left: 20%;
  bottom: -2px;
  border: 2px solid var(--clr);
  background: #272822;
  transition: 0.2s;
}

button:hover i::after {
  width: 15px;
  left: 80%;
  animation: move 3s infinite;
}

@keyframes move {
  0% {
    transform: translateX(0);
  }
  50% {
    transform: translateX(5px);
  }
  100% {
    transform: translateX(0);
  }
}

@keyframes box {
  0% {
    box-shadow: #27272c;
  }
  50% {
    box-shadow: 0 0 25px var(--clr);
  }
  100% {
    box-shadow: #27272c;
  }
}
.status {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 5px;
  color: #abb2bf;
}
.purple-square {
  width: 20px !important;
  height: 20px !important;
  background-color: $secondary-color;
  clip-path: polygon(0 0, 0 100%, 100% 100%, 100% 0);
}
.Quote {
  margin: 62px auto;
  max-width: $layout-col2;
  position: relative;
  h3 {
    padding: 32px;
    border: 1px solid #abb2bf;
    &:last-of-type {
      width: max-content;
      margin-left: auto;
    }
  }
  img {
    position: absolute;
    &:first-of-type {
      top: -10px;
      left: 10px;
    }
    &:last-of-type {
      top: 45%;
      right: 10px;
    }
  }
}
</style>
