<template>
  <div class="container">
    <table>
      <tr class="head">
        <th>ردیف</th>
        <th>کد</th>
        <th>تاریخ و ساعت</th>
        <th>مبلغ کل</th>
        <th>وضعیت</th>
        <th>عملیات</th>
        <th>جزییات</th>
      </tr>
      <tr v-for="(order, index) in orders" :key="order.id">
        <td>{{index+1}}</td>
        <td>{{order.id}}</td>
        <td>{{order.time}}</td>
        <td>{{order.price}}</td>
        <td style="color:#2223c8">{{order.status}}</td>
        <td style="color:white;"><a class="action" href="###">{{order.action}}</a></td>
        <td><div class="img" :style="{backgroundImage : 'url(' + order.details + ')'}" @click="showDetails($event)"></div></td>
        <div class="accordion"></div>
      </tr>

    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      orders: [
        {id : "1", time : "00:00 97/2/3", price : "35000 تومان", status : "تحویل شده", action : "پرداخت",
        details: "https://cdn3.iconfinder.com/data/icons/smoothfill-arrow/30/arrow_127-down-bottom-download-direction-512.png"},
        {id : "2", time : "00:00 97/2/3", price : "35000 تومان", status : "تحویل شده", action : "پرداخت",
        details: "https://cdn3.iconfinder.com/data/icons/smoothfill-arrow/30/arrow_127-down-bottom-download-direction-512.png"},
        {id : "3", time : "00:00 97/2/3", price : "35000 تومان", status : "تحویل شده", action : "پرداخت",
        details: "https://cdn3.iconfinder.com/data/icons/smoothfill-arrow/30/arrow_127-down-bottom-download-direction-512.png"},
        {id : "4", time : "00:00 97/2/3", price : "35000 تومان", status : "تحویل شده", action : "پرداخت",
        details: "https://cdn3.iconfinder.com/data/icons/smoothfill-arrow/30/arrow_127-down-bottom-download-direction-512.png"},
        {id : "5", time : "00:00 97/2/3", price : "35000 تومان", status : "تحویل شده", action : "پرداخت",
        details: "https://cdn3.iconfinder.com/data/icons/smoothfill-arrow/30/arrow_127-down-bottom-download-direction-512.png"}
      ],
    }
  },

  methods: {
    showDetails: function(event){
      var n = event.target;
      console.log(n);
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
}

.head {
  background-color: #d7d7d7;
  width: 14.3%;
  text-align: center;
}

tr {
  background-color: rgb(184, 222, 247);
  border-bottom: solid 2px white;
  height: 30px;
}

td, th {
  width: 14.3%;
  text-align: center;
}

.action {
  color: white;
  padding: 1px 30px;
  background-color: #2223c8;
  border-radius: 20px;
  text-decoration: none;
}

.img {
  background-position: center;
  background-size: cover;
  width: 20px;
  height: 20px;
  margin-left: auto;
  margin-right: auto;
}

.accordion {
  width: 80%;
  height: 200px;
  position: relative;
  display: none;
  background-image: url("https://www.w3schools.com/howto/img_nature_wide.jpg");
}

.show {display:block;}

</style>
