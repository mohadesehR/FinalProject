<template>
  <div>
    <div class ="header">
      <h2>Clothster</h2>
      <div class="itemPlaceHolder">
        <a href="/profile"><div class="item"><p><b>نام کاربر</b></p><img class="icon" src="https://cdn3.iconfinder.com/data/icons/smoothfill-arrow/30/arrow_127-down-bottom-download-direction-512.png"/></div></a>
        <a href="/shoppingCart"><div class="item"><p>سبد خرید</p><img class="icon" src="https://cdn2.iconfinder.com/data/icons/web/512/Shopping_Cart-512.png"/></div></a>
        <div class="item"><p>پیگیری سفارش</p><img class="icon" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQg8fFzOB4UkXlfZ2rqjMzOkqQ3pf8HwddOmP4J96liVT2hez-m_g"/></div>
      </div>
      <div class="processbar">
        <b-img :src="require('../static/img2.png')" style="width:100%;height:auto;margin-bottom:100px;" />
        <div class="cost">
          <p>هزینه ارسال</p><br/>
          <p style="color:blue; font-size:20px;float:left">3000</p><br/>
          <p style="float:left;color:blue">تومان</p>
        </div>
        <AddressContainer/>
        <a href="/checkAddress" class="btn" style="font-size:15px;">اضافه کردن آدرس جدید</a>
      </div>
      <div class="selectTime">
        <p>زمان دریافت سفارش</p><br/>
        <select class="times">
          <option value="">روز دریافت - تاریخ - ساعت</option>
          <option value="">روز دریافت - تاریخ - ساعت</option>
          <option value="">روز دریافت - تاریخ - ساعت</option>
          <option value="">روز دریافت - تاریخ - ساعت</option>
        </select><br/>
        <a href="/checkAddress" class="btn" style="margin-left:0px;margin-right:700px;">ثبت و مرحله بعد</a>
      </div>
    </div>
    <Footer/>
  </div>
</template>

<script>
import AddressContainer from '@/components/AddressContainer'
import Footer from '@/components/Footer'
export default {
  components: {
    AddressContainer,
    Footer
  },

}
</script>

<style scoped>
.header {
    font-family:Shabnam;
    margin-right:auto;
    margin-left:auto;
    width : 1140px;
    height : auto;
}
    .header h2 {
        text-align:center;
    }
    .header p {
        text-align:right;
        font-size:25px;
        color:#676767;
        margin-bottom:-15px;
        font-size:15px;
        float:right;
        margin-top: 0px;
    }

.itemPlaceHolder{
  height:35px;
}

.item {
  float:right;
  margin-left:2px;
  width: auto;
  height: auto;
  padding: 5px;
  margin-right: 5px;
  text-align: center;
}

.icon {
  width: 20px;
  height: 20px;
  float: right;
  margin-left:2px;
}

.processbar {
  width: 100%;
  height: auto;
}

.btn {
  text-decoration: none;
  color: white;
  background-color: #2223c8;
  padding: 5px 50px;
  border: solid 1px #2223c8;
  border-radius: 25px;
  margin-top: 25px;
  margin-left: 130px;
}

.cost {
  text-align: center;
  width: 120px;
  height: 100px;
  margin: 0px auto;
}

.times {
  width: 450px;
  height: auto;
  direction: rtl;
  padding: 5px;
  color: #676767;
  margin-top: 15px;
}

.selectTime {
  width: 78%;
  height: auto;
  text-align: right;
  margin: 10px auto;
  color: #676767;
}
</style>
