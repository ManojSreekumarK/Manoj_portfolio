<template>
  <section id="skills">
    <div>
      <h2><span>#</span>Skills</h2>
      <hr />
    </div>
    <div class="content">
      <div class="design">
        <RectangleDesign class="rectangle" />
        <RectangleDesign class="rectangle" />
        <LogoDesign class="logo" />
        <DotsDesign class="dots1" />
        <DotsDesign class="dots2" />
      </div>

      <div class="skill-data">
        <div class="card">
          <header><h4>Others</h4></header>
          <p>HTML CSS SCSS REST</p>
        </div>
        <div>
          <div class="card">
            <header><h4>Databases</h4></header>
            <p>SQlite PostgreSQL Mongo</p>
          </div>
          <div class="card">
            <header><h4>Frameworks</h4></header>
            <p>Vue Angular React Svelte</p>
          </div>
        </div>
        <div>
          <div class="card">
            <header><h4>Languages</h4></header>
            <p>Python Javascript Typescript C C++ Java</p>
          </div>
          <div class="card">
            <header><h4>Tools</h4></header>
            <p>
              Figma Git Linux destros(OS) Photoshop Illustrator After Effects Bubble.io(LCNC)
              Mendix(LCNC) Webflow(LCNC)
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import RectangleDesign from '@/components/designcomponent/RectangleDesign.vue'
import LogoDesign from '@/components/designcomponent/LogoDesign.vue'
import DotsDesign from '@/components/designcomponent/DotsDesign.vue'
</script>

<style scoped lang="scss">
@import '@/styles/varables';
#skills {
  width: $layout-col1;
  max-width: $max-width;
  margin: 84px auto;
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
.content {
  display: flex;
  justify-content: center;
}
.design {
  display: none;
  position: relative;
  @media (min-width: 1024px) {
    display: block;
  }
}
.rectangle {
  position: absolute;
  opacity: 0.5;
  &:nth-child(1) {
    left: 160px;
    top: 290px;
  }
  &:nth-child(2) {
    left: -110px;
    top: 25px;
    width: 52px;
    height: 52px;
  }
}
.logo {
  left: 25px !important;
  top: 210px !important;
}
.dots1 {
  left: 215px;
  top: 330px;
}
.dots2 {
  left: -185px;
  top: 148px;
}
.skill-data {
  margin-top: 50px;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 20px;
  .card {
    border: 1px solid #abb2bf;
    width: 196px;
    height: fit-content;
    margin-bottom: 20px;
    p {
      padding: 10px;
    }
  }
  header {
    border-bottom: 1px solid #abb2bf;
    padding: 10px;
  }
}
</style>
