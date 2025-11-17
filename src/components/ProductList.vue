<script>
import ProductCard from './ProductCard.vue'
export default {
  data() {
    return {
      products: [
        {
          title: 'tailored stretch',
          photo: '/public/photos/1photo.svg',
          collection: 'turn it up pants',
          price: 180,
          newStatus: true,
          favoriteStatus: false,
        },
        {
          title: 'technical silk',
          photo: '/public/photos/2photo.png',
          collection: 'Make A Splash',
          price: 120,
          newStatus: false,
          favoriteStatus: false,
        },
        {
          title: 'cool weave',
          photo: '/public/photos/3photo.png',
          collection: 'Anywhere Dress',
          price: 210,
          newStatus: true,
          favoriteStatus: true,
        },
      ],
    }
  },
  components: {
    ProductCard,
  },
  methods: {
    isFavorite(n) {
      this.products[n].favoriteStatus = !this.products[n].favoriteStatus
    },
  },
}
</script>

<template>
  <div class="product-list">
    <ul>
      <li v-for="(product, index) in products" :key="index">
        <ProductCard
          :title="product.title"
          :photo="product.photo"
          :collection="product.collection"
          :price="product.price"
          :newStatus="product.newStatus"
          :favoriteStatus="product.favoriteStatus"
          :id="index"
          @isFavorite="isFavorite"
        />
      </li>
    </ul>
  </div>
</template>

<style scoped>
/* selectors */
ul {
  list-style: none;
}
li {
  grid-column: span 4;
}
ul,
li {
  display: inherit;
  grid-template-columns: subgrid;
  gap: inherit;
  padding: 0;
}

/* classes */
.product-list ul {
  grid-column: 1/-1;
  margin: 0;
  grid-row-gap: 42px;
}
</style>
