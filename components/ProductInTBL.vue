<template>
  <div class="container">
    <div class="img" :style="{backgroundImage : 'url(' + image + ')'}"></div>
    <div class="info">
      <p>{{brand}}</p>
      <p style="font-size:12px">{{name}} {{name}} {{name}}</p>
      <p style="font-size:8px">رنگ: {{color}}</p>
      <p style="font-size:8px">سایز: {{size}}</p>
      <p style="font-size:8px">کد کالا: {{id}}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['image', 'id', 'brand', 'name', 'color', 'size']
}
</script>

<style scoped>
.container {
  width: 320px;
  height: 100px;
}

.img {
  width: 100px;
  height: 80px;
  margin: 10px 10px;
  float: right;
  background-position: center;
  background-size: cover;
}

.info {
  width: 150px;
  height: 80px;
  margin: 10px 10px;
  float: right;
  direction: rtl;
  text-align: right;
}

p {
  margin-bottom: 0px;
  color: #676767;
}
</style>

