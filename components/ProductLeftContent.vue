<template>
  <div class="leftContent">
    <h2>{{brand}}</h2>
    <p style="color:#676767; font-size:25px;">{{name}}{{name}}{{name}}</p>
    <p dir="rtl">رنگ:  {{color}}
    <div class="box">
      <div class="right"><p>{{priceWithoutOff}}</p></div>
      <div class="left"><p>{{priceWithOff}}</p></div>
    </div>
    <div class="imgs">
      <div v-for="i in images" :key="i.src">
        <img class="smalls" :src="i.src"/>
      </div>
    </div>
    <select class="size">
      <option value="انتخاب کنید">انتخاب کنید</option>
      <option v-for="size in sizes" :key="size" value="">{{size}}</option>
    </select>
    <p style="float: right; margin-right:10px; margin-top:5px;">راهنمای سایز</p>
    <div class="addToCart">
      <div class="addKey">
        <div class="fa fa-shopping-basket" style="font-size:15px; float:right; margin:15px 30px 5px 0px;"></div>
        <p style="float:right; margin-right:5px;">افزودن به سبد خرید</p>
      </div>
      <div class="heart"></div>
    </div>
    <div class="myDiv">
      <div class="icon" style="background-image:url(https://www.iconsdb.com/icons/preview/color/676767/action-undo-xl.png)"></div>
      <div class="text">ضمانت هفت روز بازگشت کالا</div>
      <div class="icon" style="background-image:url(https://www.iconsdb.com/icons/preview/color/676767/truck-2-xl.png)"></div>
      <div class="text">تحویل رایگان</div>
      <div class="icon" style="background-image:url(https://www.iconsdb.com/icons/preview/color/676767/shield-xl.png)"></div>
      <div class="text">ضمانت اصل بودن کالا</div>
    </div>
    <h4>ویژگی ها</h4>
    <Properties :properties="properties"/>
  </div>
</template>

<script>
import Properties from '@/components/Properties'
export default {
  components: {
    Properties,
  },

  props: ['id', 'images', 'brand', 'name', 'off', 'priceWithOff', 'priceWithoutOff', 'sizes', 'color', 'properties']
}
</script>

<style scoped>
.leftContent {
  font-size: 15px;
  width: 600px;
  height: 800px;
  margin-right: 20px;
  float: right;
  text-align: right;
}

.right {
  text-decoration: line-through;
  text-decoration-color: #a7a7a7;
  color: #a7a7a7;
  float: right;
}

.left {
  color: deeppink;
  float: right;
  margin-right: 20px;
}

.box {
  height: 30px;
  margin-left: auto;
  margin-right: auto;
  text-align: right;
}

.imgs {
  width: 100%;
  height: 130px;
  float: right;
}

.smalls {
  width: 80px;
  height: 120px;
  float: right;
  margin-left: 5px;
  border: solid 1px #676767;
}

.size {
  float: right;
  width: 200px;
  height: auto;
  direction: rtl;
  padding: 5px;
}

.addToCart{
  width: 100%;
  height: 50px;
  margin-top: 200px;
  color: #ffffff;
}

.addKey {
  width: 200px;
  height: 50px;
  display: block;
  float: right;
  background-color: rgb(211, 2, 82);
  color: #ffffff;
  text-align: center;
  line-height: 50px;
}

.heart {
  background-image: url("https://www.iconsdb.com/icons/preview/color/676767/favorite-4-xxl.png");
  background-position: center;
  background-size: cover;
  float:right;
  margin-right:5px;
  width:50px;
  height:50px;
}

.heart:hover {
  background-image: url("https://www.iconsdb.com/icons/preview/soylent-red/favorite-5-xl.png");
}

.myDiv {
  width: 100%;
  height: 40px;
  margin: 20px 0px;
}

.icon {
  float: right;
  width: 40px;
  height: 40px;
  background-position: center;
  background-size: cover;
}

.text {
  float: right;
  width: auto;
  height: 40px;
  font-size: 13px;
  padding: 20px 10px;
  color: #676767;
}

</style>
