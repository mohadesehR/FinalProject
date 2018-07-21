<template>
  <div>
    <p>{{title}}</p>
    <table>
      <tr>
        <td class="arrow1" @click="right">
        </td>
        <td>
          <div class="cardSlider" :id="id">
            <a href="/products" v-for="productCard in productCards" :key="productCard.name">
            <ProductCard
              :image = "productCard.image"
              :brand = "productCard.brand"
              :name = "productCard.name"
              :off = "productCard.off"
              :priceWithOff = "productCard.priceWithOff"
              :priceWithoutOff = "productCard.priceWithoutOff" />
            </a>
          </div>
        </td>
        <td class="arrow2" @click="left">
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
import ProductCard from '@/components/ProductCard'
export default {

  props: ['id', 'title', 'productCards'],

  components: {
    ProductCard
  },

  data() {
    return {

    }
  },


  methods: {
    right: function() {
      document.getElementById(this.id).scrollLeft -= 150;
    },

    left: function() {
      document.getElementById(this.id).scrollLeft += 150;
    }
  }
}
</script>

<style scoped>
.cardSlider{
  width: 1300px;
  height: 260px;
  margin-left: auto;
  margin-right: auto;
  overflow: auto;
  white-space: nowrap;
}

a {
  display: inline-block;
}

p {
  color: #676767;
  font-size: 35px;
  text-align: right;
  margin-right: 110px;
}

.arrow1 {
  width: 10%;
  background-image: url("https://www.iconsdb.com/icons/preview/color/676767/arrow-88-xl.png");
  background-position: center;
  background-repeat: no-repeat;
  cursor: pointer;
}

.arrow1:hover {
  background-image: url("https://www.iconsdb.com/icons/preview/color/2223C8/arrow-88-xl.png");
}

.arrow2 {
  width: 10%;
  background-image: url("https://www.iconsdb.com/icons/preview/color/676767/arrow-24-xl.png");
  background-position: center;
  background-repeat: no-repeat;
  cursor: pointer;
}

.arrow2:hover {
  background-image: url("https://www.iconsdb.com/icons/preview/color/2223C8/arrow-24-xl.png");
}
</style>
