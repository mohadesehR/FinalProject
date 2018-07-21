<template>
  <div class="container" id="container">
    <div v-for="p in properties" :key="p.text">
      <div class="line">
        <div class="circle"></div><p class="p">{{p}}</p>
      </div>
    </div>
    <div class="btn" id="btn" @click="clicked">
      <p id="more">نمایش بیشتر</p>
      <div class="arrow" id="arrow"></div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['properties'],

  data() {
    return {
      count : 1,
    }
  },

  methods: {
    init: function(){
      var lines = document.getElementsByClassName("line");
      var op = 1;
      var i;

      for (i = 2 ; i < lines.length ; i++) {
        lines[i].style.opacity = op;
        op -= 0.3;
      }
    },

    clicked: function() {
      if (this.count%2 == 1)
        this.showMore();
      else
        this.showLess();

      this.count++;
    },

    showMore: function() {
      //console.log("Hi Hani");
      var lines = document.getElementsByClassName("line");
      var op = 1;
      var i;

      for (i = 2 ; i < lines.length ; i++) {
        lines[i].style.opacity = op;
      }

      document.getElementById("container").style.height = 33*lines.length + 'px';
      document.getElementById("btn").style.marginTop = "0px";
      document.getElementById("more").innerHTML = "نمایش کمتر";
      document.getElementById("arrow").style.backgroundImage = "url('https://www.iconsdb.com/icons/preview/color/676767/arrow-141-xl.png')";
      var inc = 800 + 33*lines.length - 200;
      document.getElementById("content").style.height = inc + 'px';
    },

    showLess: function() {
      //console.log("Hi Hani");
      var lines = document.getElementsByClassName("line");
      var op = 1;
      var i;

      for (i = 2 ; i < lines.length ; i++) {
        lines[i].style.opacity = op;
        op -= 0.3;
      }

      document.getElementById("container").style.height = "200px";
      document.getElementById("btn").style.marginTop = "-200px";
      document.getElementById("more").innerHTML = "نمایش بیشتر";
      document.getElementById("arrow").style.backgroundImage = "url('https://www.iconsdb.com/icons/preview/color/676767/arrow-204-xl.png')";
      document.getElementById("content").style.height = "800px";
    }

  },

  mounted() {
    this.init()
  }
}
</script>

 <style scoped>
.container {
  width: 100%;
  height: 200px;
  margin-top: 20px;
}

.line {
  width: 100%;
  height: 33px;
}

.circle {
  margin: 5px;
  width: 15px;
  height: 15px;
  background-image: url("https://www.iconsdb.com/icons/preview/color/676767/circle-xl.png");
  background-size: cover;
  background-position: center;
  float: right;
}

.p {
  margin: 3px;
  float: right;
}

.btn {
  width: 100%;
  height: 50px;
  text-align: center;
  font-size: 15px;
  position: relative;
  margin-top: -200px;
}

.arrow {
  background-image: url("https://www.iconsdb.com/icons/preview/color/676767/arrow-204-xl.png");
  background-size: cover;
  background-position: center;
  width: 25px;
  height: 25px;
  margin: 0px auto;
}

#more {
  margin: 0px;
}
 </style>
