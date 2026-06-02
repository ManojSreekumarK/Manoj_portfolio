<script setup lang="ts">
import NavBar from '@/components/Nav/NavBar.vue'
import FooterSection from '@/components/footer/FooterSection.vue'
import { RouterView } from 'vue-router'
</script>

<template>
  <NavBar />
  <RouterView />
  <FooterSection />
</template>

<style lang="scss">
@import './styles/varables';
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  border: none;
  font-family: 'Fira Code', monospace;
}
body {
  background: $primary-color;
}

a {
  text-decoration: none;
}

li {
  list-style: none;
}
button {
  background: none;
  font: inherit;
  border: none;
  cursor: pointer;
}
h1 {
  font-weight: 600;
  font-size: 20px;
  line-height: 30px;
  color: #ffffff;
}
h2 {
  font-weight: 500;
  font-size: 28px;
  line-height: 31px;
  color: #ffffff;
}
h3 {
  font-weight: 500;
  font-size: 24px;
  line-height: 31px;
  color: #ffffff;
}
h4 {
  font-weight: 500;
  font-size: 20px;
  line-height: 31px;
  color: #ffffff;
}
h5 {
  font-weight: 500;
  font-size: 18px;
  line-height: 31px;
  color: #ffffff;
}
p {
  font-weight: 400;
  font-size: 10px;
  line-height: 25px;
  color: #abb2bf;
  @media (min-width: 490px) {
    font-size: 12px;
  }
}
</style>
