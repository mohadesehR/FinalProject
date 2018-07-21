<template>
  <div class="slide-container">
    <div class="myImage">
      <img :src="images[currentIndex]"/>
    </div>

    <a class="prev" @click="prev">&#10094;</a>
    <a class="next" @click="next">&#10095;</a>

    <div style="text-align:center">
      <div v-bind:key="images.size">
        <span class="dot"></span>
      </div>
    </div>


  </div>
</template>

<script>
export default {
  data() {
    return {
      images : ['https://www.w3schools.com/howto/img_mountains_wide.jpg',
                    'https://www.w3schools.com/howto/img_nature_wide.jpg',
                    'https://www.w3schools.com/howto/img_snow_wide.jpg',
                    'https://www.w3schools.com/howto/img_lights_wide.jpg'],
      currentIndex : 0,
      timer: null
    }
  },

 /* asyncData() {
    return new Promise((resolve, reject)=> {
      setTimeout(()=>{
        resolve({
          images : ['https://www.w3schools.com/howto/img_mountains_wide.jpg',
                    'https://www.w3schools.com/howto/img_nature_wide.jpg',
                    'https://www.w3schools.com/howto/img_snow_wide.jpg',
                    'https://www.w3schools.com/howto/img_lights_wide.jpg']
        })
      }, 1500)
    })
  },*/

  mounted: function(){
    console.log("currentIndex = " + currentIndex);
      this.startRotation;
  },

  methodes: {
    startRotation: function() {
      this.timer = setInterval(this.next, 3000);
    },

    next: function() {
      this.currentNumber += 1
    },

    prev: function() {
      this.currentNumber -= 1
    }
  }
}
</script>


<style scoped>
.slide-container {
  width: 99%;
  height: 400px;
  margin-right: auto;
  margin-left: auto;
  margin-top: 80px;
  border: solid 1px #d7d7d7;
}

.myImage {
  width: 1300px;
  height: 92%;
  margin-right: auto;
  margin-left: auto;
  border: solid 1px #676766;
  margin-top: 10px;
}



.prev, .next {
  cursor: pointer;
  position: absolute;
  top: 310px;
  width: auto;
  padding: 16px;
  color: white;
  font-weight: bold;
  font-size: 18px;
  transition: 0.6s ease;
  border-radius: 0 3px 3px 0;
}

.next {
  right: 0;
  border-radius: 3px 0 0 3px;
}

.dot {
  cursor: pointer;
  height: 15px;
  width: 15px;
  margin: 0 2px;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
  transition: background-color 0.6s ease;
}

.active, .dot:hover {
  background-color: #717171;
}

.fade {
  -webkit-animation-name: fade;
  -webkit-animation-duration: 1.5s;
  animation-name: fade;
  animation-duration: 1.5s;
}

@-webkit-keyframes fade {
  from {opacity: .4}
  to {opacity: 1}
}

@keyframes fade {
  from {opacity: .4}
  to {opacity: 1}
}

</style>

