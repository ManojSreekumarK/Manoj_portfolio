<template>
  <section id="about">
    <div>
      <h2><span>#</span>about-me</h2>
      <hr />
    </div>
    <main>
      <div class="content">
        <p>
          Hello, i’m Manoj! <br /><br />I’m a front-end developer based in Kerala, India. I can
          develop responsive websites from scratch and raise them into modern user-friendly web
          experiences.<br /><br />
          Transforming my creativity and knowledge into a websites has been my passion for over a
          year. I have been helping various clients to establish their presence online. I always
          strive to learn about the newest technologies and frameworks.
        </p>
      </div>
      <div class="image">
        <img src="@/assets/homepage/Manoj.png" alt="Manoj Avatar image 2" />
      </div>
    </main>
  </section>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
@import '@/styles/varables';
#about {
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
  @media (min-width: 1024px) {
    gap: 200px;
  }

  .content {
    width: 500px;
    margin: 60px 0;
    p {
      line-height: 30px;
      text-align: justify;
    }
  }
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
</style>
