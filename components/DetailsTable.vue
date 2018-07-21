<template>
  <div class="container">
    <table>
      <tr class="head">
        <th width="40%">مشخصات محصول</th>
        <th width="22%">تعداد</th>
        <th width="33%">قیمت</th>
        <th width="5%"></th>
      </tr>
      <tr v-for="p in products" :key="p.id">
        <td>
        <ProductInTBL
          :image=p.image
          :id=p.id
          :brand=p.brand
          :name=p.name
          :color=p.color
          :size=p.size />
        </td>
        <td>
          <div class="plus" @click="inc"></div><div class="num" :id="p.id">{{p.count}}</div><div class="minus" @click="dec"></div>
        </td>
        <td>
          <PriceInTBL
          :priceWithoutOff=p.priceWithoutOff
          :off=p.Off />
        </td>
        <td style="background-color:rgb(213, 213, 255);"><img width="30px" src="https://www.materialui.co/materialIcons/navigation/close_grey_192x192.png"/></td>
      </tr>
    </table>
  </div>
</template>

<script>
import ProductInTBL from '@/components/ProductInTBL'
import PriceInTBL from '@/components/PriceInTBL'
export default {
  components: {
    ProductInTBL,
    PriceInTBL
  },
  data() {
    return{
      products: [
        {
          id: "1",
          brand: "nike",
          name: "کفش",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          color: "سفید",
          size: "46",
          priceWithoutOff: "100.000",
          Off: "20.000",
          count: "1"
        },
        {
          id: "2",
          brand: "nike",
          name: "کفش",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          color: "سفید",
          size: "46",
          priceWithoutOff: "100.000",
          Off: "20.000",
          count: "1"
        }
      ],
    }

  },

  methods: {
    inc: function() {

    },

    dec: function() {

    }
  }
}
</script>

<style scoped>
.container {
  width: 100%;
  height: auto;
}

table {
  width: 80%;
  height: auto;
  direction: rtl;
  margin-left: auto;
  margin-right: auto;
  text-align: center;
}

.head {
  background-color: rgb(213, 213, 255);
  height: 50px;
  border: solid 1px;
  border-top: none;
}

td, th {
  border: solid 1px;
  border-top: none;
}

.plus {
  width: 30px;
  height: 30px;
  background-image: url("https://www.iconsdb.com/icons/preview/gray/plus-4-xxl.png");
  background-position: center;
  background-size: cover;
  float: right;
  margin-right: 30px;
}

.minus {
  width: 30px;
  height: 30px;
  background-image: url("https://www.iconsdb.com/icons/preview/gray/minus-8-xxl.png");
  background-position: center;
  background-size: cover;
  float: right;
}

.num {
  width: 50px;
  text-align: center;
  height: 30px;
  float: right;
}

</style>
