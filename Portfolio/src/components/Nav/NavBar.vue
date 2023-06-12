<template>
  <div class="share">
    <div class="share-line"></div>
    <div class="menu">
      <input type="checkbox" href="#" class="menu-open" name="menu-open" id="menu-open" />
      <label class="menu-open-button" for="menu-open">
        <img src="src/assets/navbar/icons8-connect.svg" />
      </label>
      <a href="#" class="menu-item"><img src="src/assets/navbar/icons8-github.svg" alt="" /></a>
      <a href="#" class="menu-item"><img src="src/assets/navbar/icons8-linkedin.svg" alt="" /></a>
      <a href="#" class="menu-item"><img src="src/assets/navbar/freelancer-icon .svg" alt="" /></a>
    </div>
  </div>
  <nav>
    <img src="src/assets/navbar/Manoj_logo-removebg-preview.png" />
    <ul>
      <li>
        <a><span>#</span>home</a>
      </li>
      <li>
        <a><span>#</span>works</a>
      </li>
      <li>
        <a><span>#</span>about me</a>
      </li>
      <li>
        <a><span>#</span>contact</a>
      </li>
      <li>
        <a
          >EN
          <svg viewBox="0 0 10 7" fill="none" xmlns="http://www.w3.org/2000/svg">
            <line
              x1="0.707107"
              y1="1.29289"
              x2="5.70711"
              y2="6.29289"
              stroke="#eb7132"
              stroke-width="2"
            />
            <line
              x1="4.29289"
              y1="6.29289"
              x2="9.29289"
              y2="1.29289"
              stroke="#eb7132"
              stroke-width="2"
            />
          </svg>
        </a>
      </li>
    </ul>
  </nav>
</template>

<script setup lang="ts"></script>

<style lang="scss" scoped>
@import 'src/styles/varables';
nav img {
  width: 72px;
  height: 21px;
}
nav {
  max-width: $layout-col1;
  margin: 32px auto;
}
span {
  color: $secondary-color;
}

nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  ul {
    display: flex;
    align-items: center;
    gap: 32px;
  }
}
li {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 50px;
  position: relative;
  z-index: 0;
}
nav a {
  color: #eb7132;
  svg {
    width: 10px;
    height: 5px;
  }
  &:last-of-type {
    display: flex;
    align-items: center;
  }
  &::after {
    content: '';
    position: absolute;
    z-index: 2;
    width: 50%;
    height: 100%;
    top: 0%;
    left: 0%;
    transform: translate(0, -50%) scaleY(0);
    transition: transform 1s ease;
    mix-blend-mode: difference;

    clip-path: polygon(0 70%, 100% 70%, 100% 30%, 0 30%, 0 0, 60% 0%, 60% 20%, 0% 20%);

    background-color: #eb7132;
  }
  &:hover::after {
    transform: translate(0, 0%) scaleY(1);
  }
  &::before {
    content: '';
    position: absolute;
    z-index: 2;
    width: 50%;
    height: 100%;
    bottom: 0%;
    right: 0%;
    transform: translate(0, 50%) scaleY(0);
    transition: transform 1s ease;
    mix-blend-mode: difference;

    clip-path: polygon(100% 30%, 0% 30%, 0% 70%, 100% 70%, 100% 100%, 40% 100%, 40% 80%, 100% 80%);

    background-color: #eb7132;
  }
  &:hover::before {
    transform: translate(0%, 0%) scaleY(1);
  }
}
@media only screen and (min-width: 1500px) {
  nav {
    width: 1500px;
  }
}
.share {
  position: absolute;
  top: 0;
  left: 40px;
}
.share-line {
  border-right: 2px solid #abb2bf;
  height: 191px;
  margin-left: 18px;
  width: 2px;
}
.menu-item {
  background: #090e16;
  border-radius: 100%;
  width: 38px;
  height: 38px;

  position: absolute;
  top: 8px;
  color: $color_1;
  text-align: center;
  line-height: 52px;
  transform: translate3d(0, 0, 0);
  transition: transform ease-out 200ms;
  transition-duration: 180ms;
  img {
    height: 25px;
    width: 25px;
  }
}
.menu-open-button {
  background: #090e16;
  border-radius: 100%;
  width: 38px;
  height: 38px;
  // margin-left: -13px;
  position: absolute;
  top: 8px;
  color: $color_1;
  text-align: center;
  line-height: 52px;
  transform: translate3d(0, 0, 0);
  transition: transform ease-out 200ms;
  z-index: 2;
  transition-duration: 400ms;
  transform: scale(1.1, 1.1) translate3d(0, 0, 0);
  cursor: pointer;
  &:hover {
    transform: scale(1.2, 1.2) translate3d(0, 0, 0);
  }
  img {
    height: 25px;
    width: 25px;
  }
}
.menu-open {
  display: none;
  &:checked {
    + {
      .menu-open-button {
        transition-timing-function: linear;
        transition-duration: 200ms;
        transform: scale(0.8, 0.8) translate3d(0, 0, 0);
      }
    }
    ~ {
      .menu-item {
        transition-timing-function: cubic-bezier(0.935, 1.33);
        &:nth-child(3) {
          transition-duration: 180ms;
          transform: translate3d(44.08361px, -23.99997px, 0);
        }
        &:nth-child(4) {
          transition-duration: 280ms;
          transform: translate3d(48.9466px, 27.52414px, 0);
        }
        &:nth-child(5) {
          transition-duration: 380ms;
          transform: translate3d(1.9466px, 52.47586px, 0);
        }
      }
    }
  }
}
.menu {
  position: absolute;
  width: 380px;
  height: 250px;
  box-sizing: border-box;
}
</style>
