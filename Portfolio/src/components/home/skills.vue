<template>
  <section id="skills">
    <div>
      <h2>
        <span>#</span>Skills
        <hr />
      </h2>
    </div>
  </section>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
@import '@/styles/varables';
#skills {
  max-width: $layout-col1;
  margin: 84px auto;
  h2 {
    display: flex;
    gap: 5px;
    align-items: center;
    hr {
      width: 511px;
      height: 1px;
      border-top: 1px solid $secondary-color;
    }
    span {
      color: $secondary-color;
    }
  }
}
</style>
