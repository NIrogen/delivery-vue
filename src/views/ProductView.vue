<script setup>
import { store } from '../store/index'

const getUrl = (name) => {
  return new URL(`../assets/images/goods/${name}.jpg`,  import.meta.url)
}

</script>

<template>
  <section class="products">
    <div class="container">
      <div class="products-wrapper" id="goods-container">
        <div class="products-card" v-for="good in store.goods" :key="good.id">
          <div class="products-card--image">
            <img :src="getUrl(good.img)" alt="good1">
          </div>
          <div class="products-card--description">
            <div class="products-card--description_row">
              <h5 class="products-card--description__name">
                {{ good.name }}
              </h5>
            </div>
            <div class="products-card--description_row">
              <p class="products-card--description__text">
                {{ good.desc }}
              </p>
            </div>
            <div class="products-card--description_row">
              <div class="products-card--description_controls">
                <button class="btn btn-primary">
                  В корзину
                  <img src="../assets/images/WhiteCart.png" alt="WhiteCart">
                </button>
                <span class="products-card--description_controls__price">
                  {{ good.price }} ₽
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
