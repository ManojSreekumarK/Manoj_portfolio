<template>
  <section class="Projects">
    <div>
      <h2>
        <span>#</span>Projects
        <hr />
      </h2>
      <div>
        <p>View all &#8594;</p>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
@import '@/styles/varables';
.Projects {
  max-width: $layout-col1;
  margin: 84px auto;
  div:nth-child(1) {
    display: flex;
    justify-content: space-between;
  }
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
