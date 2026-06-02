<template>
  <nav>
    <div class="share">
      <div class="share-line"></div>
      <div class="menu">
        <input type="checkbox" href="#" class="menu-open" name="menu-open" id="menu-open" />
        <label class="menu-open-button" for="menu-open">
          <img src="@/assets/navbar/icons8-connect.svg" alt="connect icon" />
        </label>
        <a href="https://github.com/ManojSreekumarK" class="menu-item"
          ><img src="@/assets/navbar/icons8-github.svg" alt="github"
        /></a>
        <a href="https://www.linkedin.com/in/manoj-sreekumar" class="menu-item"
          ><img src="@/assets/navbar/icons8-linkedin.svg" alt="linkedln"
        /></a>
        <a href="https://www.freelancer.in/u/manojsreekumar20?sb=t" class="menu-item"
          ><img src="@/assets/navbar/freelancer-icon.svg" alt="freelancer"
        /></a>
      </div>
    </div>
    <img src="@/assets/navbar/Manoj_logo-removebg-preview.png" alt="Manoj logo" />
    <ul>
      <li>
        <a href="#"><span>#</span>home</a>
      </li>
      <li>
        <a href="#Projects"><span>#</span>works</a>
      </li>
      <li>
        <a href="#skills"><span>#</span>skills</a>
      </li>
      <li>
        <a href="#about"><span>#</span>about</a>
      </li>
    </ul>
  </nav>
</template>

<script setup lang="ts"></script>

<style lang="scss" scoped>
@import '@/styles/varables';
nav > img {
  width: 72px;
  height: 21px;
  @media (min-width: 768px) {
    margin-left: 100px;
  }
}
nav {
  max-width: $max-width;
  width: $layout-col1;
  margin: 32px auto;
  position: relative;
}
span {
  color: $secondary-color;
}

nav {
  display: flex;
  align-items: center;
  justify-content: center;
  @media (min-width: 768px) {
    justify-content: space-between;
  }
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
nav {
  li > a {
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

      clip-path: polygon(
        100% 30%,
        0% 30%,
        0% 70%,
        100% 70%,
        100% 100%,
        40% 100%,
        40% 80%,
        100% 80%
      );

      background-color: #eb7132;
    }
    &:hover::before {
      transform: translate(0%, 0%) scaleY(1);
    }
  }
}
.share {
  position: absolute;
  left: 0;
  top: -32px;
}
.share-line {
  border-right: 2px solid #eb7132;
  height: 38px;
  margin-left: 18px;
  width: 2px;
  @media (min-width: 768px) {
    height: 70px;
  }
  @media (min-width: 1024px) {
    height: 100px;
  }
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
}
@media screen and (max-width: 768px) {
  nav ul {
    display: none;
  }
}
</style>
