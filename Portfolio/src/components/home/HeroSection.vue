<template>
  <section id="hero">
    <div>
      <h1>I am <span>Manoj Sreekumar</span> and I am a <span>front-end developer</span></h1>
      <p>
        Welcome to my portfolio! I'm a passionate frontend developer with a love for creating
        visually appealing and interactive web experiences.
      </p>
      <button style="--clr: #c778dd"><span>Contact me!!</span><i></i></button>
    </div>
    <div class="hero-image">
      <LogoDesign class="logo" />
      <dots class="hero-dots" />
      <img src="@/assets/homepage/ManojSreekumar.png" alt="Manoj avatar" />
      <div class="status">
        <div class="purple-square"></div>
        <span>Currently working for Pitsolutions</span>
      </div>
    </div>
  </section>
  <div class="Quote">
    <img src="@/assets/homepage/Quote.svg" alt="opening quotes" />
    <h3>On the other side of the screen, it all looks so easy</h3>
    <img src="@/assets/homepage/Quote.svg" alt="closing quotes" />
    <h3>-"Tron" (1982)</h3>
  </div>
</template>

<script setup lang="ts">
import LogoDesign from '@/components/designcomponent/LogoDesign.vue'
import dots from '@/components/designcomponent/DotsDesign.vue'
</script>

<style lang="scss" scoped>
@import '@/styles/varables';
#hero {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  width: $layout-col1;
  max-width: $max-width;
  gap: 30px;
  margin: 95px auto;
  @media (min-width: 1024px) {
    gap: 100px;
  }

  & > div:last-of-type {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
    max-width: 275px;
  }
  & > div:first-of-type {
    width: 100%;
    max-width: 525px;
  }
}
h1 {
  @media (min-width: 490px) {
    font-size: 26px;
  }
  span {
    color: $secondary-color;
  }
}
p {
  @media (min-width: 490px) {
    font-size: 15px;
  }
  margin: 12px 0 24px;
  text-align: justify;
}
.status {
  width: 185px;
  height: 37px;
  background: #282c33;
  border: 1px solid #abb2bf;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 5px;
  color: #abb2bf;
  span {
    font-size: 12px;
  }
  @media (min-width: 490px) {
    width: 285px;
  }
}
.hero-image {
  position: relative;
  img {
    z-index: 8;
    width: 200px;
    height: 210px;
    @media (min-width: 490px) {
      width: 300px;
      height: 310px;
    }
  }
}
button {
  position: relative;
  background: #444;
  color: #fff;
  text-decoration: none;
  text-transform: uppercase;
  border: none;
  letter-spacing: 1.6px;
  font-size: 10px;
  padding: 12.8px 32px;
  transition: 0.2s;
  @media (min-width: 490px) {
    font-size: 15px;
  }
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

.purple-square {
  width: 30px !important;
  height: 20px !important;
  background-color: $secondary-color;
  clip-path: polygon(0 0, 0 100%, 100% 100%, 100% 0);
}
.Quote {
  margin: 62px auto;
  width: $qoute-layout1;
  max-width: 460px;
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

.hero-dots {
  top: 130px;
  left: 95px;
  z-index: 9;
  @media (min-width: 490px) {
    top: 230px;
    left: 95px;
  }
}

.logo {
  top: 100px !important;
  left: 0 !important;
}
.Quote {
  & * {
    font-size: 0.7em !important;
  }
  h3 {
    padding: 15px !important;
  }
}
</style>
