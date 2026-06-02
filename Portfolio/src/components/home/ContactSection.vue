<template>
  <section id="contact">
    <div>
      <h2><span>#</span>contact</h2>
      <hr />
    </div>
    <main>
      <div class="content">
        <p>
          I’m interested in freelance opportunities. However, if you have other request or question,
          don’t hesitate to contact me.
        </p>
      </div>
      <div class="card">
        <div class="canvas-wrapper">
          <a href="mailto:manojsreekumar2000@gmail.com" class="canvas">
            <div class="canvas_border">
              <svg>
                <defs>
                  <linearGradient id="grad-orange" x1="0%" y1="0%" x2="100%" y2="0%">
                    <stop offset="0%" style="stop-color: rgb(253, 137, 68); stop-opacity: 1"></stop>
                    <stop
                      offset="100%"
                      style="stop-color: rgb(153, 75, 23); stop-opacity: 1"
                    ></stop>
                  </linearGradient>
                  <linearGradient id="grad-red" x1="0%" y1="0%" x2="100%" y2="0%">
                    <stop offset="0%" stop-color="#D34F48"></stop>
                    <stop offset="100%" stop-color="#772522"></stop>
                  </linearGradient>
                </defs>
                <rect
                  id="rect-grad"
                  class="rect-gradient"
                  fill="none"
                  stroke="url(#grad-orange)"
                  stroke-linecap="square"
                  stroke-width="4"
                  stroke-miterlimit="30"
                  width="100%"
                  height="100%"
                ></rect>
              </svg>
            </div>
            <div class="canvas_img-wrapper">
              <img class="canvas_img" src="@/assets/homepage/email-100.png" alt="email" />
            </div>
            <div class="canvas_copy canvas_copy--left">
              <span class="canvas_copy_subtitle">Message Me</span>
              <strong class="canvas_copy_title">say</strong>
              <strong class="canvas_copy_title">hello</strong>
              <span class="canvas_copy_details">here</span>
            </div>
          </a>
          <a href="https://www.linkedin.com/in/manoj-sreekumar" class="canvas">
            <div class="canvas_border">
              <svg>
                <defs>
                  <linearGradient id="grad-orange" x1="0%" y1="0%" x2="100%" y2="0%">
                    <stop offset="0%" style="stop-color: rgb(253, 137, 68); stop-opacity: 1"></stop>
                    <stop
                      offset="100%"
                      style="stop-color: rgb(153, 75, 23); stop-opacity: 1"
                    ></stop>
                  </linearGradient>
                  <linearGradient id="grad-red" x1="0%" y1="0%" x2="100%" y2="0%">
                    <stop offset="0%" stop-color="#D34F48"></stop>
                    <stop offset="100%" stop-color="#772522"></stop>
                  </linearGradient>
                </defs>
                <rect
                  id="rect-grad"
                  class="rect-gradient"
                  fill="none"
                  stroke="url(#grad-orange)"
                  stroke-linecap="square"
                  stroke-width="4"
                  stroke-miterlimit="30"
                  width="100%"
                  height="100%"
                ></rect>
              </svg>
            </div>
            <div class="canvas_img-wrapper">
              <img class="canvas_img" src="@/assets/homepage/linkedin.svg" alt="linkedin" />
            </div>
            <div class="canvas_copy">
              <span class="canvas_copy_subtitle">Message Me</span>
              <strong class="canvas_copy_title">say</strong>
              <strong class="canvas_copy_title">hello</strong>
              <span class="canvas_copy_details">here</span>
            </div>
          </a>
        </div>
      </div>
    </main>
  </section>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
@import '@/styles/varables';
#contact {
  width: $layout-col1;
  max-width: $max-width;
  margin: 125px auto;
  & > div:nth-child(1) {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 5px;
    @media (min-width: 570px) {
      margin: 0 auto;
    }
  }
  h2 {
    display: flex;
    gap: 5px;
    align-items: center;
    span {
      color: $secondary-color;
    }
  }
  hr {
    width: 50%;
    height: 1px;
    border-top: 1px solid $secondary-color;
  }
}
main {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 60px;
  @media (min-width: 1024px) {
    gap: 280px;
  }

  .content {
    max-width: 280px;
    margin-top: 60px;
    p {
      line-height: 30px;
      text-align: justify;
    }
  }
  .card {
    margin-top: 50px;
    -webkit-animation: fade-in 3s ease-in-out forwards;
    animation: fade-in 3s ease-in-out forwards;
    .canvas-wrapper {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: center;
      height: 100%;
      gap: 45px;
    }
    // .canvas-wrapper .canvas + .canvas {
    //   margin-left: 40px;
    // }

    .canvas {
      position: relative;
      display: block;
      width: 130px;
      height: 130px;
      padding: 20px;
      color: inherit;
      text-decoration: none;
    }

    .canvas_border {
      position: absolute;
      top: 40px;
      left: -40px;
      height: 100%;
      width: 100%;
      z-index: 0;
    }
    .canvas_border svg {
      height: 100%;
      width: 100%;
    }

    .rect-gradient {
      stroke-dasharray: 2000;
      stroke-dashoffset: 2000;
      -webkit-animation: erase-line 1s ease-in-out forwards;
      animation: erase-line 1s ease-in-out forwards;
    }

    .canvas_img-wrapper {
      position: absolute;
      display: flex;
      align-items: center;
      justify-content: center;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      transform: rotate(-10deg) skew(-10deg);
      overflow: hidden;
      background: #767a83;
    }

    .canvas_img {
      transform: scale3d(0.9, 0.9, 0.9);
      opacity: 0.3;
      max-width: 200px;
      width: 100px;
      max-height: 200px;
    }

    .canvas_copy {
      position: absolute;
      bottom: 0;
      left: 85%;
      text-transform: uppercase;
      color: $secondary-color;
      z-index: 100;
    }

    .canvas_copy--left {
      left: -26%;
    }

    .canvas_copy_title {
      font-size: 26px;
      display: block;
      transform: translateX(-80px);
      transition: all 0.75s cubic-bezier(0.68, -0.55, 0.265, 1.55) 0s;
      color: white;
    }
    .canvas_copy_title:nth-child(1) {
      transition-delay: 0.1s;
    }
    .canvas_copy_title:nth-child(2) {
      transition-delay: 0.2s;
    }

    .canvas_copy_subtitle {
      display: block;
      transform: rotate(270deg) translateY(-100%) translateX(calc(-100% - 80px));
      transform-origin: top left;
      position: absolute;
      left: 0;
      top: 8px;
      font-size: 12px;
      font-weight: 900;
      transition: all 0.75s cubic-bezier(0.68, -0.55, 0.265, 1.55) 0.35s;
    }

    .canvas_copy_details {
      display: block;
      transition: all 0.75s cubic-bezier(0.68, -0.55, 0.265, 1.55) 0.14s;
      transform: translateX(-80px);
    }

    .canvas_border,
    .canvas_img-wrapper,
    .canvas_img {
      transition: all 0.25s ease-in-out 0s;
    }

    .canvas_border,
    .canvas_img-wrapper {
      transform: rotate(-10deg) skew(-10deg);
    }

    .canvas_copy_title,
    .canvas_copy_subtitle,
    .canvas_copy_details {
      opacity: 0;
    }

    .canvas:hover .canvas_copy_title,
    .canvas:hover .canvas_copy_subtitle,
    .canvas:hover .canvas_copy_details,
    .canvas:hover .canvas_img {
      opacity: 1;
    }
    .canvas:hover .canvas_border,
    .canvas:hover .canvas_img-wrapper {
      transform: rotate(-14deg) skew(-14deg) scale(0.96);
    }
    .canvas:hover .canvas_img {
      transform: scale3d(1, 1, 1);
    }
    .canvas:hover .canvas_copy_title,
    .canvas:hover .canvas_copy_details {
      transform: translateX(0);
    }
    .canvas:hover .canvas_copy_subtitle {
      transform: rotate(270deg) translateY(-100%) translateX(-100%);
    }
    .canvas:hover .rect-gradient {
      -webkit-animation: draw-line 3s cubic-bezier(0.19, 1, 0.22, 1) forwards;
      animation: draw-line 3s cubic-bezier(0.19, 1, 0.22, 1) forwards;
    }

    @-webkit-keyframes draw-line {
      from {
        stroke-dashoffset: 2000;
      }
      to {
        stroke-dashoffset: 0;
      }
    }

    @keyframes draw-line {
      from {
        stroke-dashoffset: 2000;
      }
      to {
        stroke-dashoffset: 0;
      }
    }
    @-webkit-keyframes erase-line {
      from {
        stroke-dashoffset: 0;
      }
      to {
        stroke-dashoffset: 2000;
      }
    }
    @keyframes erase-line {
      from {
        stroke-dashoffset: 0;
      }
      to {
        stroke-dashoffset: 2000;
      }
    }
    @-webkit-keyframes fade-in {
      from {
        opacity: 0;
      }
      to {
        opacity: 1;
      }
    }
    @keyframes fade-in {
      from {
        opacity: 0;
      }
      to {
        opacity: 1;
      }
    }
  }
}
</style>
