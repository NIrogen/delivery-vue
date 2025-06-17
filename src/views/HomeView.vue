<script setup>
import { store } from '../store/index'

const getUrl = (name) => {
  return new URL(`../assets/images/products/${name}.jpg`,  import.meta.url)
}


</script>

<template>
  <section class="banner">
    <div class="container">
      <div class="banner-item">
        <h2 class="banner-item--title">
          Онлайн-сервис <br> доставки еды на дом
        </h2>
        <p class="banner-item--subtitle">
          Блюда из любимого ресторана привезет курьер в перчатках, маске и с антисептиком
        </p>
      </div>
    </div>
  </section>
  <section class="products">
    <div class="container">
      <div class="products-header">
        <h3 class="products-header--title">
          Рестораны
        </h3>
        <input type="text" class="products-header--search" placeholder="Поиск блюд и ресторанов">
      </div>
      <div class="products-wrapper" id="rests-container">
        <router-link 
        
        class="products-card" 
        v-for="rest in store.rests" 
        :key="rest.id"
        :to="`/rest?id=${rest.id}`" 
        >
          <div class="products-card--image">
            <img :src="getUrl(rest.img)" alt="ПЦ">
          </div>
          <div class="products-card--description">
            <div class="products-card--description_row">
              <h4 class="products-card--description__title">{{ rest.title }}</h4>
              <div class="products-card--description__bage">{{ rest.time }} мин</div>
            </div>
            <div class="products-card--description_row">
              <div class="products-card--description_info">
                <div class="products-card--description_info__raiting">
                  <img src="../assets/images/star.svg" alt="star">{{ rest.rating }}
                </div>
                <div class="products-card--description_info__price">От {{ rest.price }}р</div>
                <div class="products-card--description_info__group">{{ rest.type }}</div>
              </div>
            </div>
          </div>
        </router-link>
      </div>
    </div>
  </section>
</template>
