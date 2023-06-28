<template>
  <section id="Projects">
    <div>
      <h2>
        <span>#</span>Projects
        <hr />
      </h2>
      <div>
        <p>View all &#8594;</p>
      </div>
    </div>
    <div class="cards">
      <div class="card">
        <div class="card_head">
          <div class="wrapper">
            <img src="@/assets/homepage/brandscard.png" class="cover-image" />
          </div>
          <img src="@/assets/homepage/brandslogo.svg" class="title" />
          <img src="@/assets/homepage/brandsch.svg" class="character" />
        </div>
        <div class="card_content">
          <header><p>html css javascript</p></header>
          <section>
            <h3>Brands.io</h3>
            <p>Exploring different brand identities dummy website</p>
            <button class="glow-on-hover" type="button">Live &#8594;</button>
          </section>
        </div>
      </div>

      <div class="card">
        <div class="card_head">
          <div class="wrapper">
            <img src="@/assets/homepage/tastenowcard.png" class="cover-image" />
          </div>
          <img src="@/assets/homepage/Tastenowlogo.svg" class="title" />
          <img src="@/assets/homepage/tastenowch.svg" class="character" />
        </div>
        <div class="card_content">
          <header><p>html css javascript</p></header>
          <section>
            <h3>Taste Now</h3>
            <p>Online Food Delivery dummy website</p>
            <button class="glow-on-hover" type="button">Live &#8594;</button>
          </section>
        </div>
      </div>
      <div class="card">
        <div class="card_head">
          <div class="wrapper">
            <img src="@/assets/homepage/denticscard.png" class="cover-image" />
          </div>
          <img src="@/assets/homepage/Logo.svg" class="title" />
          <img src="@/assets/homepage/Illustration.svg" class="character" />
        </div>
        <div class="card_content">
          <header><p>html css javascript</p></header>
          <section>
            <h3>Dentics</h3>
            <p>Dental Clinic landing page dummy website</p>
            <button class="glow-on-hover" type="button">Live &#8594;</button>
          </section>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
@import '@/styles/varables';
#Projects {
  max-width: $layout-col1;
  margin: 84px auto;
  & > div:nth-child(1) {
    display: flex;
    justify-content: space-between;
  }
  h2 {
    display: flex;
    gap: 5px;
    align-items: center;
    hr {
      width: 511px;
      height: 1px;
      border-top: 1px solid $secondary-color;
    }
    span {
      color: $secondary-color;
    }
  }
}

.cards {
  margin: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 100px;
}
.card_head {
  width: 325px;
  height: 300px;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: flex-end;
  padding: 0 36px;
  perspective: 2500px;
}
.card:hover {
  .wrapper {
    transform: perspective(900px) translateY(-5%) rotateX(25deg) translateZ(0);
    box-shadow: 2px 35px 32px -8px rgba(0, 0, 0, 0.75);
    -webkit-box-shadow: 2px 35px 32px -8px rgba(0, 0, 0, 0.75);
    -moz-box-shadow: 2px 35px 32px -8px rgba(0, 0, 0, 0.75);
    &::before {
      opacity: 1;
    }
    &::after {
      height: 120px;
    }
  }
  .title {
    transform: translate3d(0%, -30px, 100px);
  }
  .character {
    opacity: 1;
    transform: translate3d(0%, -52%, 100px);
  }
}
.cover-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.wrapper {
  transition: all 0.5s;
  position: absolute;
  width: 100%;
  z-index: -1;
  &::before {
    content: '';
    opacity: 0;
    width: 100%;
    height: 80px;
    transition: all 0.5s;
    position: absolute;
    left: 0;
    top: 0;
    height: 100%;
    background-image: linear-gradient(
      to top,
      transparent 46%,
      rgba(12, 13, 19, 0.5) 68%,
      rgba(12, 13, 19) 97%
    );
  }
  &::after {
    content: '';
    opacity: 0;
    width: 100%;
    height: 80px;
    transition: all 0.5s;
    position: absolute;
    left: 0;
    bottom: 0;
    opacity: 1;
    background-image: linear-gradient(
      to bottom,
      transparent 46%,
      rgba(12, 13, 19, 0.5) 68%,
      rgba(12, 13, 19) 97%
    );
    opacity: 1;
  }
}
.title {
  width: 200px;
  margin-bottom: 20px;
  transition: transform 0.5s;
}
.character {
  width: 90%;
  opacity: 0;
  transition: all 0.5s;
  position: absolute;
  z-index: -1;
}
.card_content {
  width: 325px;

  border: 1px solid #abb2bf;
  header {
    border-bottom: 1px solid #abb2bf;
    padding: 5px;
  }
  section {
    padding: 16px;
    p {
      margin: 16px 0;
    }
  }
}
$color_1: #fff;
$color_2: #000;

@keyframes glowing {
  0% {
    background-position: 0 0;
  }
  50% {
    background-position: 400% 0;
  }
  100% {
    background-position: 0 0;
  }
}
.glow-on-hover {
  width: 100px;
  height: 30px;
  border: none;
  outline: none;
  color: $color_1;
  background: #282c33;
  border: 1px solid #abb2bf;
  cursor: pointer;
  position: relative;
  z-index: 0;

  &:before {
    content: '';
    background: linear-gradient(
      45deg,
      #ff0000,
      #ff7300,
      #fffb00,
      #48ff00,
      #00ffd5,
      #002bff,
      #7a00ff,
      #ff00c8,
      #ff0000
    );
    position: absolute;
    top: -2px;
    left: -2px;
    background-size: 400%;
    z-index: -1;
    filter: blur(5px);
    width: calc(100% + 4px);
    height: calc(100% + 4px);
    animation: glowing 20s linear infinite;
    opacity: 0;
    transition: opacity 0.3s ease-in-out;
  }
  &:active {
    color: $color_2;
    &:after {
      background: transparent;
    }
  }
  &:hover {
    &:before {
      opacity: 1;
    }
  }
  &:after {
    z-index: -1;
    content: '';
    position: absolute;
    width: 100%;
    height: 100%;
    background: #282c33;
    left: 0;
    top: 0;
  }
}
</style>
