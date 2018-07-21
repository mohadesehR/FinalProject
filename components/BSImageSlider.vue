<template>
  <div class="slide-container">
    <b-carousel class="myImage"
                controls
                indicators
                v-model="slide"
                @sliding-start="onSlideStart"
                @sliding-end="onSlideEnd"
    >

    <div v-for="i in images" :key="i.src">
      <b-carousel-slide :img-src="i.imgSrc">
      </b-carousel-slide>

    </div>
    </b-carousel>

  </div>
</template>

<script>
export default {
  data() {
    return {
      slide: 0,
      sliding: null,
      images : [
            {
              imgSrc : "https://file.digistyle.com/digistyle/image/webstore/banner/1397/4/23/07637461_set1.jpg"
            },
            {
              imgSrc : "https://file.digistyle.com/digistyle/image/webstore/banner/1397/4/26/c2bf9a4e_set1.jpg"
            },
            {
              imgSrc : "https://file.digistyle.com/digistyle/image/webstore/banner/1397/4/27/192ba7e0_set1.jpg"
            },
            {
              imgSrc : "https://file.digistyle.com/digistyle/image/webstore/banner/1397/4/27/d6b6dd12_set1.jpg"
            }
          ]
    }
  },

  asyncData() {
    return new Promise((resolve, reject)=> {
      setTimeout(() => {
        resolve({
          images : [
            {
              imgSrc : "https://file.digistyle.com/digistyle/image/webstore/banner/1397/4/23/07637461_set1.jpg"
            },
            {
              imgSrc : "https://file.digistyle.com/digistyle/image/webstore/banner/1397/4/26/c2bf9a4e_set1.jpg"
            },
            {
              imgSrc : "https://file.digistyle.com/digistyle/image/webstore/banner/1397/4/27/192ba7e0_set1.jpg"
            },
            {
              imgSrc : "https://file.digistyle.com/digistyle/image/webstore/banner/1397/4/27/d6b6dd12_set1.jpg"
            }
          ]
        })

      }, 1500)
    })
  },

  methods: {
    onSlideStart (slide) {
      this.sliding = true
    },
    onSlideEnd (slide) {
      this.sliding = false
    }
  }
}
</script>

<style scoped>
.slide-container {
  width: 99%;
  height: auto;
  margin-right: auto;
  margin-left: auto;
  margin-top: 80px;
  border: solid 1px #d7d7d7;
}

.myImage {
  width: 1300px;
  height: auto;
  margin-right: auto;
  margin-left: auto;
  border: solid 1px #676766;
  margin-top: 10px;
  margin-bottom: 10px;
}

.img {
  width: 100%;
  height: 100%;
}

</style>
