<template>
  <div>
    <table>
      <tr>
        <td class="arrow1" @click="right">
        </td>
        <td>
          <div class="brandSlider" id="brandSlider">
            <div class="brand" v-for="brandCard in brandCards" :key="brandCard.name">
              <BrandCard
                :name="brandCard.name"
                :url="brandCard.url"
                :image="brandCard.image" />
              </div>
          </div>
        </td>
        <td class="arrow2" @click="left">
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
import BrandCard from '@/components/BrandCard'
export default {

  components: {
    BrandCard
  },

  props: ['brandCards'],

  data() {
    return {

    }
  },

    methods: {
    right: function() {
      document.getElementById("brandSlider").scrollLeft -= 600;
    },

    left: function() {
      document.getElementById("brandSlider").scrollLeft += 600;
    }
  }
}
</script>

<style scoped>
.brandSlider{
  width: 1300px;
  height: 350px;
  margin-left: auto;
  margin-right: auto;
  overflow: auto;
  white-space: nowrap;
}

p {
  color: #676767;
  font-size: 35px;
  text-align: right;
  margin-right: 110px;
}

.brand {
  display: inline-block;
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
