<script setup lang="ts">
import NavBar from '@/components/Nav/NavBar.vue'
import { RouterView } from 'vue-router'
const components = {
  'nav-bar': NavBar
}
</script>

<template>
  <nav-bar></nav-bar>
  <RouterView></RouterView>
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
  font-size: 32px;
  line-height: 42px;
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
p {
  font-weight: 400;
  font-size: 16px;
  line-height: 25px;
  color: #abb2bf;
}
</style>
