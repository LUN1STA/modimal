<script>
export default {
  data() {
    return {
      liked: '/public/icons/LikedIcon.svg',
      notLiked: '/public/icons/FavoriteHeaderIcon.svg',
    }
  },
  props: ['id', 'title', 'photo', 'collection', 'price', 'newStatus', 'favoriteStatus'],
  methods: {
    isFavorite() {
      this.$emit('isFavorite', this.id)
    },
  },
}
</script>

<template>
  <div class="product-card">
    <div v-if="newStatus" class="new-product chip--sm body--sm">New</div>
    <img
      :src="favoriteStatus ? liked : notLiked"
      alt="like"
      class="like-product"
      @click="isFavorite"
    />
    <img :src="photo" alt="product photo" class="product-card__photo" />
    <div class="product-card__information">
      <div class="product-card__information__feature">
        <h6 class="product-card__information__feature__title">{{ title }}</h6>
        <p class="product-card__information__feature__collection body--md">{{ collection }}</p>
        <div class="product-card__information__feature__color">
          <div class="product-card__information__feature__color--left"></div>
          <div class="product-card__information__feature__color--center"></div>
          <div class="product-card__information__feature__color--right"></div>
        </div>
      </div>
      <h6 class="product-card__information__price">${{ price }}</h6>
    </div>
  </div>
</template>

<style>
/* classes */
.product-card {
  height: 540px;
  position: relative;
  display: inherit;
  grid-template-columns: subgrid;
  column-gap: inherit;
}
.new-product {
  position: absolute;
  top: 24px;
  left: 24px;
}
.like-product {
  position: absolute;
  top: 24px;
  right: 24px;
}
.product-card,
img.product-card__photo,
.product-card__information {
  grid-column: 1/5;
}
.product-card__information {
  display: inherit;
  grid-template-columns: subgrid;
  column-gap: inherit;
  padding: 5.5px 8px;
}
.product-card__information__feature {
  display: inherit;
  grid-column: 1/3;
  grid-template-rows: repeat(3, 1fr);
  column-gap: 8px;
}
.product-card__information__feature__color {
  display: flex;
  justify-items: flex-start;
}
.product-card__information__feature__color > * {
  width: 25px;
  height: 25px;
  border-radius: 50%;
  background-color: blueviolet;
  margin-right: 7px;
}
.product-card__information__feature > * {
  margin: 0;
}
.product-card__information__price {
  grid-column: 3/5;
  justify-self: flex-end;
}
</style>
