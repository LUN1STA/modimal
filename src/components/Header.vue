<template>
  <header>
    <div id="green__line" class="overline--sm">Enjoy Free Shipping On All Orders</div>
    <div class="header-block">
      <div id="logo"><img src="/public/Logo.svg" alt="logo" /></div>
      <div class="header-block-pages">
        <ul class="body--lg">
          <li>Collection</li>
          <li>New In</li>
          <li><a href="#">Modiweek</a></li>
          <li>Plus Size</li>
          <li>Sustainability</li>
        </ul>
      </div>
      <div class="header-block-icons">
        <ul>
          <li>
            <img src="/public/icons/SearchHeaderIcon.svg" alt="" />
          </li>
          <li>
            <img src="/public/icons/ProfileHeaderIcon.svg" alt="" />
          </li>
          <li>
            <img src="/public/icons/FavoriteHeaderIcon.svg" alt="" />
          </li>
          <li>
            <img src="/public/icons/BagHeaderIcon.svg" alt="" />
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script>
export default {}
</script>

<style scoped>
/* selectors */
ul {
  list-style: none;
  width: 100%;
}

/* classes */
.header-block {
  padding: 0 120px;
  height: 80px;
  align-items: center;
  display: grid;
  grid-template-columns: 2fr 1fr 6fr 1fr 2fr;
}
.header-block:has(+ #logo) {
  justify-items: center;
}
.header-block-pages {
  grid-column: 3 / 4;
  padding: 0 4px;
}
.header-block-pages ul {
  padding: 0;
  display: flex;
  justify-content: space-between;
}
.header-block-pages ul > li,
.header-block-pages ul > li a {
  color: rgba(64, 64, 64, 1);
  text-decoration: none;
}
.header-block-icons {
  grid-column: 5;
  padding: 0 8px;
}
.header-block-icons ul {
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: space-between;
}

/* id */
#green__line {
  background: rgba(90, 109, 87, 1);
  width: 100%;
  height: 30px;
  text-align: center;
  color: white;
  align-content: center;
}
#logo {
  align-content: center;
  padding: 0;
  height: 100%;
}
#logo img {
  height: 46px;
  width: 100%;
  padding: 16px 0;
}
</style>
