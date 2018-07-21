<template>
  <div>
    <LogedInNavbar/>
    <div class="userForm">
      <UserInfo/>
    </div>
    <div class="box">
      <p>آدرس ها</p>
      <img class="icon" src="https://cdn3.iconfinder.com/data/icons/smoothfill-arrow/30/arrow_127-down-bottom-download-direction-512.png"/><br/>
      <AddressContainer/>
      <a href="/checkAddress" class="btn" style="font-size:15px;">اضافه کردن آدرس جدید</a>
    </div>
    <div class="box">
      <p>سفارشات</p>
      <img class="icon" src="https://cdn3.iconfinder.com/data/icons/smoothfill-arrow/30/arrow_127-down-bottom-download-direction-512.png"/><br/>
      <OrderTable/>
    </div>

    <Footer/>
  </div>
</template>

<script>
import LogedInNavbar from '@/components/LogedInNavbar'
import UserInfo from '@/components/UserInfo'
import AddressContainer from '@/components/AddressContainer'
import OrderTable from '@/components/OrderTable'
import Footer from '@/components/Footer'
export default {
  components: {
    LogedInNavbar,
    AddressContainer,
    OrderTable,
    UserInfo,
    Footer
  }
}
</script>

<style scoped>
.userForm {
  width: 100%;
  height: 450px;
}

.box {
  width: 100%;
  height: auto;
  margin: 20px;
  color: #676767;
}

p {
  margin-right: 190px;
  float: right;
  direction: rtl;
}

.icon {
  width: 20px;
  height: 20px;
  float: right;
  margin-left:2px;
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

</style>
