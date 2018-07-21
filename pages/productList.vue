<template>
  <div>
    <LogedInNavbar/>
    <Menubar/>
    <div class="content">
      <div class="right">
        <Filter1/>
        <Filter2/>
        <Filter3/>
      </div>
      <div class="left">
        <ProductList/>
      </div>
    </div>
    <Footer/>
  </div>
</template>

<script>
import LogedInNavbar from '@/components/LogedInNavbar'
import Menubar from '@/components/Menubar'
import Filter1 from '@/components/Filter1'
import Filter2 from '@/components/Filter2'
import Filter3 from '@/components/Filter3'
import ProductList from '@/components/ProductList'
import Footer from '@/components/Footer'
export default {
  components: {
    LogedInNavbar,
    LogedInNavbar,
    Filter1,
    Filter2,
    Filter3,
    ProductList,
    Footer
  },

}
</script>

<style scoped>
.content {
  width: 1140px;
  height: 1050px;
  margin: 100px auto 20px auto;
}

.right {
  width: 260px;
  height: auto;
  float: right;
}

.left {
  width: 830px;
  height: auto;
  float: right;
  margin-right: 50px;
}
</style>
