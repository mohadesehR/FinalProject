<template>
  <div class="productCard">
    <div class="productImage" :style="{backgroundImage : 'url(' + image + ')'}">
      <div class="off"><p>{{off}}</p></div>
    </div>
    <div class="productInfo">
      <p>{{brand}}</p>
      <p style="color:#a7a7a7;">{{name}}</p>
      <div class="box">
        <div class="right"><p>{{priceWithoutOff}}</p></div>
        <div class="left"><p>{{priceWithOff}}</p></div>
      </div>
      <p style="color:deeppink; text-align:center;">تومان</p>
    </div>
  </div>
</template>

<script>
export default {
    props : ['id', 'image', 'brand', 'name', 'off', 'priceWithOff', 'priceWithoutOff']
}
</script>

<style scoped>
.productCard {
  width: 150px;
  height: 220px;
  margin-top: 10px;
  float: left;
  margin-right: 2px;
}

.productImage {
  width: 140px;
  height: 140px;
  border: solid 1px #676767;
  margin: 5px;
  background-position: center;
  background-size: cover;
}

.productInfo {
  width: 140px;
  height: auto;
  margin: 5px;
  text-align: center;
  font-size: 10px;
}

p {
  margin: 0px;
}

.right {
  text-decoration: line-through;
  text-decoration-color: #a7a7a7;
  color: #a7a7a7;
  float: right;
  margin-right: 20px;
}

.left {
  color: deeppink;
  margin-left: 20px;
  float: left;
  margin-right: 10px;
}

.box {
  height: 15px;
  margin-left: auto;
  margin-right: auto;
  text-align: center;
}

.off {
  height: 30px;
  width: 35px;
  border-radius: 15px;
  color: #ffffff;
  background-color: rgb(211, 2, 82);
  position: relative;
  padding-top: 4px;
  padding-left: 3px;
}
</style>
