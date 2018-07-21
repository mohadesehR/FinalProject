<template>
  <div>
    <LogedInNavbar/>
    <BSImageSlider/>
    <ItemSlider title="محبوب ترین ها" id="slider1" :productCards="this.populareProducts"/>
    <div class="img" :style="{backgroundImage : 'url(' + bnr1 + ')'}"></div>
    <ItemSlider title="جدیدترین ها" id="slider2" :productCards="this.newProducts"/>
    <div class="img" :style="{backgroundImage : 'url(' + bnr2 + ')'}"></div>
    <BrandSlider :brandCards="this.brands"/>
    <Footer/>
  </div>
</template>

<script>
import LogedInNavbar from '@/components/LogedInNavbar'
import BSImageSlider from '@/components/BSImageSlider'
import ItemSlider from '@/components/ItemSlider'
import BrandSlider from '@/components/BrandSlider'
import Footer from '@/components/Footer'
export default {

  props : ['populareProducts', 'newProducts', 'brands', 'bnr1', 'bnr2'],

  components : {
    LogedInNavbar,
    BSImageSlider,
    ItemSlider,
    BrandSlider,
    Footer
  }

}
</script>

<style scoped>
.img {
  width: 100%;
  height: 350px;
  background-position: center;
  background-size: cover;
  margin: 10px 0px;
}
</style>
