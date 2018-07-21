<template>
  <div class="container">
    <h5>نام دسته</h5>
    <p style="color:#676767;float:right">مرتب سازی</p>
    <select class="orderBy">
      <option v-for="o in orderBy" :key="o" :value="o">{{o}}</option>
    </select>
    <div class="pagination">
      <div class="next" id="next" @click="next">صفحه بعد<div class="icon2"></div></div>
      صفحه {{count}} از {{max}}
      <div class="prev" id="prev" @click="previece"><div class="icon1"></div>صفحه قبل</div>
    </div>
    <div class="album" id="album">
      <a href="/products" class="links" v-for="productCard in productCards" :key="productCard.name">
        <ProductCard
          :image = "productCard.image"
          :brand = "productCard.brand"
          :name = "productCard.name"
          :off = "productCard.off"
          :priceWithOff = "productCard.priceWithOff"
          :priceWithoutOff = "productCard.priceWithoutOff" />
        <!--span class="tooltiptext"><img :src="productCard.image2"/></span-->
      </a>
    </div>
  </div>
</template>

<script>
import ProductCard from '@/components/ProductCard'
export default {
  components: {
    ProductCard,
  },

  data() {
    return {
      orderBy: ['محبوب ترین', 'جدیدترین', 'مردانه', 'زنانه', 'بچگانه'],
      productCards: [
        {
          id: "1",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "2",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "3",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "4",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "5",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "6",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "7",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "8",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "9",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "10",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "1",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "2",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "3",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "4",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "5",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "6",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "7",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "8",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "9",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "10",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          image2: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        }
    ],
    max : 0,
    count : 1
    }
  },

  mounted(){
    this.max = Math.ceil(this.productCards.length/16);
    document.getElementById("prev").style.color = "#d7d7d7";
    document.getElementById("prev").style.borderColor = "#d7d7d7";
    //console.log(this.max);
  },

  methods: {
    next: function() {
      //scroll change
      if (this.count != this.max) {
        this.count++;
        document.getElementById("album").scrollTop += 960;
      }

      if (this.count == this.max) {//disable next
        document.getElementById("next").style.color = "#d7d7d7";
        document.getElementById("next").style.borderColor = "#d7d7d7";
      }
      else {
        document.getElementById("next").style.color = "#676767";
        document.getElementById("next").style.borderColor = "#676767";
      }

      if (this.count != 1) {
        document.getElementById("prev").style.color = "#676767";
        document.getElementById("prev").style.borderColor = "#676767";
      }
    },

    previece: function() {
      //scroll change
      if (this.count != 1) {
        this.count--;
        document.getElementById("album").scrollTop -= 960;
      }
      if (this.count == 1) {//disable next
        document.getElementById("prev").style.color = "#d7d7d7";
        document.getElementById("prev").style.borderColor = "#d7d7d7";
      }
      else {
        document.getElementById("prev").style.color = "#676767";
        document.getElementById("prev").style.borderColor = "#676767";
      }

      if (this.count != this.max) {
        document.getElementById("next").style.color = "#676767";
        document.getElementById("next").style.borderColor = "#676767";
      }
    }
  }
}
</script>

<style scoped>
.container {
  width: 830px;
  height: 960px;
  margin: 0px auto;
  text-align: right;
}

.orderBy {
  width: 150px;
  height: auto;
  text-align: right;
  direction: rtl;
  float: right;
  margin-right: 10px;
}

.pagination {
  height: 27.6px;
  width: 340px;
  float: left;
}

.next, .prev {
  float: left;
  width: 110px;
  height: auto;
  color: #676767;
  border: solid 1px #676767;
  font-size: 15px;
  margin : 0px 8px;
  text-align: center;
  cursor: pointer;
}

.icon1 {
  width: 25px;
  height: 25px;
  float: right;
  background-image: url("https://www.iconsdb.com/icons/preview/color/676767/arrow-88-xl.png");
  background-size: cover;
  background-position: center;
}

.icon2 {
  width: 25px;
  height: 25px;
  float: left;
  background-image: url("https://www.iconsdb.com/icons/preview/color/676767/arrow-24-xl.png");
  background-size: cover;
  background-position: center;
}

.album {
  width: 100%;
  height: 960px;
  overflow-y: auto;
}

.links {
  display: inline-block;
  margin: 10px 15px;
}

</style>
