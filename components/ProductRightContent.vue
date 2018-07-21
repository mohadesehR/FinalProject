<template>
  <div class="rightContent">
    <div class="float">
    <div class="img1" @click="up"/>
    <div class="imgHolder" id="imgHolder">
      <div v-for="i in images" :key="i.src">
        <img class="smalls" :src="i.src"/>
      </div>
    </div>
    <div class="img2" @click="down"/>
    </div>
    <div class="big" :style="{backgroundImage : 'url(' + image.src + ')'}">
      <div class="off"><p>{{off}}</p></div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['images', 'image', 'off'],

  methods: {
    up: function() {
      document.getElementById("imgHolder").scrollTop -= 100;
    },

    down: function() {
      document.getElementById("imgHolder").scrollTop += 100;
    }
  }
}
</script>

<style scoped>
.rightContent {
  width: 455px;
  height: 800px;
  float: right;
}

.float {
  float: right;
  width: 150px;
  height: 400px;
}

.imgHolder {
  width: 150px;
  height: 400px;
  overflow: auto;
  text-align: center;
}

.smalls {
  width: 120px;
  margin: 0px 5px 5px 5px;
  height: auto;
  border: solid 1px #676767;
}

.img1 {
  background-image: url("https://www.iconsdb.com/icons/preview/color/676767/arrow-141-xl.png");
  background-position: center;
  background-repeat: no-repeat;
  width: 100%;
  height: 50px;
}

.img1:hover {
  background-image: url("https://www.iconsdb.com/icons/preview/color/2223C8/arrow-141-xl.png");
  background-position: center;
  background-repeat: no-repeat;
}

.img2 {
  background-image: url("https://www.iconsdb.com/icons/preview/color/676767/arrow-204-xl.png");
  background-position: center;
  background-repeat: no-repeat;
  width: 100%;
  height: 50px;
}

.img2:hover {
  background-image: url("https://www.iconsdb.com/icons/preview/color/2223C8/arrow-204-xl.png");
  background-position: center;
  background-repeat: no-repeat;
}

.big {
  width: 300px;
  height: 500px;
  float: right;
  border: solid 1px #676767;
  margin-right: 5px;
  background-position: center;
  background-size: cover;
}

.off {
  text-align: center;
  height: 60px;
  width: 60px;
  border-radius: 30px;
  background-color: rgb(211, 2, 82);
  position: relative;
  padding: 12px 5px;
  font-size: 28px;
}
</style>
