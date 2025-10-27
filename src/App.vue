<script setup>
import Header from './components/Header.vue'
</script>

<template>
  <Header />
  <div class="main-image">
    <img src="/public/photos/hero.svg" alt="" />
    <div class="main-image__button">
      <p>Elegance in simplicity, Earth’s harmony</p>
      <button class="button--sm button button--dark--fill">New In</button>
    </div>
  </div>
</template>

<style scoped>
.main-image {
  position: relative;
  display: inline-block;
  width: 100%;
}
.main-image img {
  width: 100%;
}
.main-image__button {
  position: absolute;
  top: 50%;
  left: 120px;
}
.main-image__button p {
  color: black;
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  font-size: 34px;
  font-style: italic;
  width: 350px;
  text-align: bottom;
}
.main-image__button button {
  width: 184px;
}
</style>
