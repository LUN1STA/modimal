<script>
import Header from './components/Header.vue'
import ProductList from './components/ProductList.vue'

export default {
  components: {
    Header,
    ProductList,
  },
}
</script>

<template>
  <Header />
  <div class="main-image">
    <img src="/public/photos/hero.svg" alt="" />
    <div class="main-image__button">
      <p>Elegance In Simplicity, Earth’s Harmony</p>
      <button class="button--sm button button--dark--fill">New In</button>
    </div>
  </div>
  <ProductList class="product-list" />
</template>

<style scoped>
.main-image {
  height: calc(100vw * 5 / 12);
}
.main-image,
.main-image__button {
  grid-column: 1/-1;
  display: inherit;
  grid-template-columns: subgrid;
  gap: inherit;
  position: relative;
}
.main-image img {
  position: absolute;
  width: 100vw;
  transform: translateX(calc(-1 * (100vw - 1224px) / 2));
}
.main-image__button {
  margin-top: calc((100vw * 5 / 12) / 2);
  grid-auto-rows: max-content;
}
.main-image__button p {
  color: black;
  font-family: 'Gill Sans Italic', sans-serif;
  font-size: 34px;
  line-height: 180%;
  text-align: start;
  grid-column: 1/4;
  margin: 0;
  height: fit-content;
}
.main-image__button button {
  margin-top: 27px;
  grid-column: 1/3;
}
.product-list {
  grid-column: 1/-1;
}
</style>
