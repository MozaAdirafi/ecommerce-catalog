<template>
  <div v-if="product">
     <div class="page-mensection-container">
      <div class="page-mensection-page-mensection">
        <img
          v-if="product.category === 'men\'s clothing'"
          src="/playground_assets/rectangle51197-asn-800h.png"
          alt="Rectangle51197"
          class="page-mensection-rectangle5"
        />
        <img
          v-else-if = "product.category === 'women\'s clothing'"
          src="/playground_assets/rectangle513-rgbb-600h.png"
          alt="Pink image"
          class="page-mensection-rectangle5"
        />

        <div class="page-mensection-group21">
          <div class="page-mensection-group7">
            <span class="page-mensection-text">
              <span>{{product.title}}</span>
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
  
  
<style scoped>
  .page-mensection-container {
    min-height: 100vh;
  }
  .page-mensection-page-mensection {
    width: 1920px;
    height: 960px;
    display: flex;
    overflow: hidden;
    position: relative;
    align-items: flex-start;
    flex-shrink: 0;
    border-color: transparent;
  }
  .page-mensection-rectangle5 {
    top: -100px;
    left: 1px;
    width: 1920px;
    height: 725px;
    position: absolute;
    border-color: transparent;
  }
  .page-mensection-group21 {
    top: 66.25030517578125px;
    left: 260px;
    width: 1399.019287109375px;
    height: 784.7496948242188px;
    display: flex;
    padding: 0;
    position: absolute;
    align-self: auto;
    box-shadow: 10px 10px 10px 5px #d4d4d4;
    box-sizing: border-box;
    align-items: flex-start;
    flex-shrink: 1;
    border-color: transparent;
    border-style: none;
    border-width: 0;
    margin-right: 0;
    border-radius: 0px 0px 0px 0px;
    margin-bottom: 0;
    flex-direction: row;
    justify-content: flex-start;
    background-color: rgba(255, 255, 255, 1);
  }
  .page-mensection-group7 {
    top: 66.29782104492188px;
    left: 581.7971801757812px;
    width: 768.6022338867188px;
    height: 665.6842651367188px;
    display: flex;
    padding: 0;
    position: absolute;
    align-self: auto;
    box-sizing: border-box;
    align-items: flex-start;
    flex-shrink: 1;
    border-color: transparent;
    border-style: none;
    border-width: 0;
    border-radius: 0px 0px 0px 0px;
    flex-direction: row;
    justify-content: flex-start;
    background-color: transparent;
  }
  .page-mensection-text {
    color: rgba(0, 38, 114, 1);
    width: 741px;
    height: auto;
    position: absolute;
    font-size: 28px;
    align-self: auto;
    font-style: Semi Bold;
    text-align: left;
    font-family: Inter;
    font-weight: 700;
    line-height: normal;
    font-stretch: normal;
    text-decoration: none;
  }
  .page-mensection-text02 {
    top: 69.00382995605469px;
    left: 0.000006581454726983793px;
    color: rgba(62, 62, 62, 1);
    width: 168px;
    height: auto;
    position: absolute;
    font-size: 18px;
    align-self: auto;
    font-style: Regular;
    text-align: left;
    font-family: Inter;
    font-weight: 400;
    line-height: normal;
    font-stretch: normal;
    text-decoration: none;
  }
  .page-mensection-text04 {
    top: 142.0667266845703px;
    left: 0.000006581454726983793px;
    color: rgba(30, 30, 30, 1);
    width: 700px;
    height: auto;
    position: absolute;
    font-size: 20px;
    align-self: auto;
    font-style: Regular;
    text-align: left;
    font-family: Inter;
    font-weight: 400;
    line-height: normal;
    font-stretch: normal;
    text-decoration: none;
  }
  .page-mensection-group3 {
    top: 69.00382995605469px;
    left: 526.323486328125px;
    width: 200.24647521972656px;
    height: 29.766366958618164px;
    display: flex;
    padding: 0;
    position: absolute;
    align-self: auto;
    box-sizing: border-box;
    align-items: center;
    flex-shrink: 1;
    border-color: transparent;
    border-style: none;
    border-width: 0;
    border-radius: 0px 0px 0px 0px;
    flex-direction: row;
    justify-content: center;
    background-color: transparent;
  }
  
  .page-mensection-text06 {
    top: 3px;
    left: -9px;
    color: rgba(62, 62, 62, 1);
    width: 61px;
    position: absolute;
    font-size: 18px;
    align-self: center;
    font-style: Regular;
    text-align: left;
    font-family: Inter;
    font-weight: 400;
    line-height: normal;
    font-stretch: normal;
    text-decoration: none;
  }
  
  .page-mensection-text08 {
    top: 531.7355346679688px;
    left: 0.000006581454726983793px;
    color: rgba(0, 38, 114, 1);
    width: 131px;
    height: auto;
    position: absolute;
    font-size: 28px;
    align-self: auto;
    font-style: Semi Bold;
    text-align: left;
    font-family: Inter;
    font-weight: 700;
    line-height: normal;
    font-stretch: normal;
    text-decoration: none;
  }
.page-mensection-group1 {
  top: 610.1712036132812px;
  left: 263.79388427734375px;
  width: 242.2787628173828px;
  height: 55.165645599365234px;
  display: flex;
  padding: 0;
  position: absolute;
  align-self: auto;
  box-sizing: border-box;
  transition: 0.3s;
  align-items: flex-start;
  flex-shrink: 1;
  border-radius: 0px 0px 0px 0px;
  flex-direction: row;
  justify-content: flex-start;
}

.page-mensection-group1:hover {
  transform: translate(0, -10px);
}
.page-mensection-text10 {
  top: 11.628026962280273px;
  left: -10.22537994384766px;
  color: rgb(255, 255, 255);
  width: 265px;
  height: auto;
  position: absolute;
  font-size: 16px;
  align-self: auto;
  font-style: Semi Bold;
  text-align: center;
  font-family: Inter;
  font-weight: 700;
  line-height: normal;
  font-stretch: normal;
  text-decoration: none;
}

.page-mensection-text10{
  background-color: #002672;
  color: #fff;
  cursor: pointer;
  padding: 10px 20px;
}

.page-mensection-text10{
  background-color: #002672;
  color: #fff;
  cursor: pointer;
  padding: 10px 20px;
  border: 2px solid #002672;
  border-radius: 0;
}

  .page-mensection-group5 {
  top: 610.5185546875px;
  left: 526.323486328125px;
  width: 242.2787628173828px;
  height: 55.165645599365234px;
  display: flex;
  padding: 0;
  position: absolute;
  align-self: auto;
  box-sizing: border-box;
  transition: 0.3s;
  align-items: flex-start;
  flex-shrink: 1;
  border-radius: 0px 0px 0px 0px;
  flex-direction: row;
  justify-content: flex-start;
  background-color: rgba(255, 255, 255, 1);
}

.page-mensection-group5:hover {
  transform: translate(0, -10px);
}

.page-mensection-group4:hover {
  transform: translate(0, -10px);
}

.page-mensection-group4 {
  left: 2px;
  width: 242.2787628173828px;
  bottom: 0px;
  height: 55.165645599365234px;
  display: flex;
  padding: 0;
  position: absolute;
  align-self: auto;
  box-sizing: border-box;
  transition: 0.3s;
  align-items: flex-start;
  flex-shrink: 1;
  border-radius: 0px 0px 0px 0px;
  flex-direction: row;
  justify-content: flex-start;
  background-color: rgba(255, 255, 255, 1);
}

.page-mensection-text11 {
  top: 11.628026962280273px;
  left: 13.530179023742676px;
  color: rgba(0, 38, 114, 1);
  width: 215px;
  height: auto;
  position: absolute;
  font-size: 16px;
  align-self: auto;
  font-style: Semi Bold;
  text-align: center;
  font-family: Inter;
  font-weight: 700;
  line-height: normal;
  font-stretch: normal;
  text-decoration: none;
}

.page-mensection-text11:hover {
  transform: translate(0, -10px);
}

.page-mensection-text13 {
  top: 11.628026962280273px;
  left: 13.530179023742676px;
  color: rgba(0, 38, 114, 1);
  width: 215px;
  height: auto;
  position: absolute;
  font-size: 16px;
  align-self: auto;
  font-style: Semi Bold;
  text-align: center;
  font-family: Inter;
  font-weight: 700;
  line-height: normal;
  font-stretch: normal;
  text-decoration: none;
}
.page-mensection-text11,
.page-mensection-text13 {
  background-color: #fff;
  color: #002672;
  cursor: pointer;
  padding: 10px 20px;
  border: 2px solid #002672;
  border-radius: 0;
}
  .page-mensection-image2 {
    top: 212px;
    left: 347px;
    width: 407px;
    height: 519px;
    position: absolute;
    border-color: transparent;
  }
  .page-mensection-vector11 {
    top: 643px;
    left: 861px;
    width: 734px;
    height: 0px;
    position: absolute;
  }
  .page-mensection-vector12 {
    top: 248px;
    left: 858px;
    width: 734px;
    height: 0px;
    position: absolute;
  }
  </style>
  