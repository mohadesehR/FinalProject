<template>
  <div class ="header">
    <h2>Clothster</h2>
    <div class="itemPlaceHolder">
      <a href="/profile"><div class="item"><p><b>نام کاربر</b></p><img class="icon" src="https://cdn3.iconfinder.com/data/icons/smoothfill-arrow/30/arrow_127-down-bottom-download-direction-512.png"/></div></a>
      <a href="/shoppingCart"><div class="item"><p>سبد خرید</p><img class="icon" src="https://cdn2.iconfinder.com/data/icons/web/512/Shopping_Cart-512.png"/></div></a>
      <div class="item"><p>پیگیری سفارش</p><img class="icon" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQg8fFzOB4UkXlfZ2rqjMzOkqQ3pf8HwddOmP4J96liVT2hez-m_g"/></div>
    <SearchBox/>
    </div>
    <Menubar/>
  </div>
</template>

<script>
import SearchBox from '@/components/SearchBox'
import Menubar from '@/components/Menubar'
export default {
  components : {
    SearchBox,
    Menubar
  },

  //props: ['username']
}
</script>


<style scoped>
.header {
    font-family:Shabnam;
    margin-right:auto;
    margin-left:auto;
    width : 1140px;
    height : 60px;
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
</style>

