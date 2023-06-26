<template>
  <div id="container">
    <div class="loader">
      <span></span>
    </div>

    <div class="loader">
      <span></span>
    </div>

    <div class="loader">
      <span></span>
    </div>

    <div class="loader">
      <span></span>
    </div>

    <div class="loader">
      <span></span>
    </div>

    <div class="loader">
      <span></span>
    </div>

    <div class="loader">
      <span></span>
    </div>

    <div class="loader">
      <span></span>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style lang="scss" scoped>
$accentColor: #c778dd;

#container {
  max-width: 400px;

  margin: 0;

  width: 52px;

  height: 52px;

  position: absolute;
}

.loader {
  height: 2px;

  background: $accentColor;

  position: relative;

  &:nth-child(1) {
    width: 52px;
  }

  &:nth-child(2) {
    width: 42px;

    top: 13px;

    left: -5px;

    transform: rotate(45deg);
  }

  &:nth-child(3) {
    width: 42px;

    top: 40px;

    left: -5px;

    transform: rotate(-45deg);
  }

  &:nth-child(4) {
    top: 53px;

    width: 52px;
  }

  &:nth-child(5) {
    width: 52px;

    top: 21px;

    left: 30px;
  }

  &:nth-child(6) {
    width: 42px;

    top: -25px;

    left: 45px;

    transform: rotate(-43deg);
  }

  &:nth-child(7) {
    width: 42px;

    top: 3px;

    left: 45px;

    transform: rotate(43deg);
  }

  &:nth-child(8) {
    top: -44px;

    left: 30px;

    width: 52px;
  }

  span {
    position: absolute;

    display: block;

    height: 2px;

    width: 5px;

    box-shadow: $accentColor 0 0 5px;

    animation: animate 2s infinite ease-in-out;

    opacity: 0;
  }

  span:nth-child(1) {
    animation-delay: 0s;
  }

  span:nth-child(2) {
    animation-delay: 0.5s;
  }

  span:nth-child(3) {
    animation-delay: 1s;
  }

  span:nth-child(4) {
    animation-delay: 1.5s;
  }
}

@keyframes animate {
  0% {
    left: 0;

    opacity: 0;
  }

  10% {
    opacity: 0;

    left: 0;
  }

  20% {
    opacity: 1;
  }

  80% {
    opacity: 1;
  }

  90% {
    opacity: 0;

    left: calc(100% - 10px);
  }

  100% {
    opacity: 0;

    left: calc(100% - 10px);
  }
}
</style>
