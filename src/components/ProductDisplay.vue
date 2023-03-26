<template>
  <div v-if="product">
     <div class="page-mensection-container">
      <div class="page-mensection-page-mensection">
        <img
          v-if="product.category === 'men\'s clothing'"
          src="../assets/images/rectangle51197-asn-800h.png"
          alt="Rectangle51197"
          class="page-mensection-rectangle5"
        />
        <img
          v-else-if = "product.category === 'women\'s clothing'"
          src="../assets/images/rectangle513-rgbb-600h.png"
          alt="Pink image"
          class="page-mensection-rectangle5"
        />

        <div class="page-mensection-group21">
          <div class="page-mensection-group7">
            <span class="page-mensection-text">
              <span>{{product.title}} ({{ product.rating.rate }}⭐)</span>
            </span>
            <span class="page-mensection-text02">
              <span>{{ product.category }}</span>
            </span>
            <span class="page-mensection-text04">
              <span>
                {{ product.description }}
              </span>
            </span>
            <span class="page-mensection-text08"><span>{{ product.price }}$</span></span>
            <div class="page-mensection-group1">
              <span class="page-mensection-text10">Buy now</span>
            </div>
            <div class="page-mensection-group5">
              <button @click="nextProduct" class="page-mensection-text11"><span>Next product</span></button>
            </div>
            <div class="page-mensection-group4">
              <button @click="previousProduct" class="page-mensection-text13"><span>Previous product</span></button>
            </div>
          </div>
        </div>
        <img
          :src="product.image" :alt="product.title"
          class="page-mensection-image2"
        />
      </div>
    </div>
  </div>
  <div v-else>
    <NotFoundPage />
  </div>
</template>

<script>
import NotFoundPage from './notfound.vue'

export default {
  name: 'PageMensection',
  data() {
    return {
      index: 1,
      product: null,
    };
  },
  methods: {
    async fetchProduct() {
      const response = await fetch(`https://fakestoreapi.com/products/${this.index}`);
      const data = await response.json();
      if (data.category === "men's clothing" || data.category === "women's clothing") {
        this.product = data;
      } else {
        this.product = null;
      }
    },
    nextProduct() {
      if (this.index === 20) {
        this.index = 1;
      } else {
        this.index++;
      }
      this.fetchProduct();
    },
    previousProduct() {
      if (this.index === 1) {
        this.index = 20;
      } else {
        this.index--;
      }
      this.fetchProduct();
    },
  },
  mounted() {
    this.fetchProduct();
  },
  components: {
    NotFoundPage,
  },
};
</script>
  
  
<style>

 @import '../assets/style/style.css'

</style>
  