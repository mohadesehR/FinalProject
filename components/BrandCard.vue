<template>
  <div class="brandCard">
    <div class="brandImage" :style="{backgroundImage : 'url(' + image + ')'}"></div>
    <div class="brandInfo">
      <p>{{name}}</p>
      <a :href=url>خرید</a>
    </div>
  </div>
</template>

<script>
export default {
  props: ['name', 'image', 'url']
}
</script>

<style scoped>
.brandCard {
  width: 602px;
  height: 302px;
  border: solid 1px #676767;
  margin: 10px;
  float: left;
}

.brandImage {
  width: 300px;
  height: 300px;
  background-position: center;
  background-size: cover;
  float: left;
  border-right: solid 1px #676767;
}

.brandInfo {
  width: 300px;
  height: 300px;
  float: left;
  text-align: center;
}

p {
  margin-top: 70px;
  font-size: 40px;
  color: #676767;
}

a {
  font-size: 20px;
  color: #ffffff;
  border: solid 1px #676767;
  background-color: #676767;
  border-radius: 30px;
  padding: 10px 20px;
  text-decoration: none;
}
</style>

