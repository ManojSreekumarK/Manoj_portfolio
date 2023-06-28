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
  height: 1px;
  background: $accentColor;
  position: relative;
  &:nth-child(1) {
    width: 51px;
  }
  &:nth-child(2) {
    width: 41px;
    top: 13.6px;
    left: -6px;
    transform: rotate(45deg);
  }
  &:nth-child(3) {
    width: 41px;
    top: 41px;
    left: -6px;
    transform: rotate(-45deg);
  }
  &:nth-child(4) {
    top: 54.5px;
    width: 52px;
  }
  &:nth-child(5) {
    width: 51px;
    top: 24.5px;
    left: 29px;
  }
  &:nth-child(6) {
    width: 43px;
    top: -20px;
    left: 45px;
    transform: rotate(-45deg);
  }
  &:nth-child(7) {
    width: 40.5px;
    top: 8px;
    left: 45px;
    transform: rotate(45deg);
  }
  &:nth-child(8) {
    top: -37.5px;
    left: 30px;
    width: 52px;
  }
  span {
    position: absolute;
    display: block;
    height: 1px;
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
