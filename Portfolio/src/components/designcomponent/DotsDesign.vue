<template>
  <div class="container">
    <div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
    </div>
    <div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
    </div>
    <div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
    </div>
    <div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
    </div>
    <div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
      <div class="dot-flashing"></div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  position: absolute;

  & > div {
    display: flex;
    gap: 10px;
    margin-top: 10px;
  }
}
.dot-flashing {
  position: relative;
  left: 100px;
  width: 4px;
  height: 4px;
  border-radius: 5px;
  background-color: #c778dd;
  color: #c778dd;
  animation: dot-flashing 1s infinite linear alternate;
  animation-delay: 0.5s;
}

@keyframes dot-flashing {
  0% {
    background-color: #c778dd;
  }
  50%,
  100% {
    background-color: rgba(152, 128, 255, 0.2);
  }
}
</style>
