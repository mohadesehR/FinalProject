<template>
  <div class="form">
    <div class="column1">
      <inputchild title = "نام و نام خانوادگی" defaultvalue = "برای مثال سارا احمدی"/>
      <inputchild title = "شماره تلفن همراه" defaultvalue = "برای مثال 09135286959"/>
      <inputchild title = "تاریخ تولد" defaultvalue = "Date Picker is here!"/>
      <div class="empty"></div>
      <inputchild title = "رمز عبور فعلی"/>
    </div>

    <div class="column2">
      <div class="img-profile-wrap">
        <p>نام کاربر</p>
        <div class="img-circle"></div>
      </div>
      <div class="gender">
        <p>جنسیت</p>
        <table>
          <tr>
            <th>مرد</th>
            <th><img width="100%" height="auto" src="https://png.icons8.com/color/260/male.png"></th>
            <th><img width="100%" height="auto" src="https://png.icons8.com/color/260/female.png"></th>
            <th>زن</th>
          </tr>
        </table>
      </div>
      <div class="empty2"></div>
      <inputchild title = "رمز عبور جدید"/>
      <div class="button">ثبت تغییرات</div>
    </div>

    <div class="column3" >
        <inputchild title = "شهر" defaultvalue = "برای مثال کرج"/>
        <inputchild title = "شماره تلفن ثابت" defaultvalue = "برای مثال 02144569786"/>
        <inputchild title = "شماره کارت 16 رقمی" defaultvalue = "اختیاری"/>
        <div class="empty"></div>
        <inputchild title = "تکرار رمز عبور جدید"/>
    </div>
  </div>
</template>

<script>
import inputchild from '@/components/inputchild'
export default {
    components: {
        inputchild
    }

}
</script>


<style scoped>
.form{
    height: 400px;
    width: 80%;
    border: #d4cccc  solid 1px;
    margin-left:auto ;
    margin-right: auto;
    margin-top: 8%;
}
.column1{
    width: 33%;
    float: right;
    height: 100%;
}

.empty {
    width: 100%;
    height: 6.5%;
}

.column2{
    width: 33%;
    float: right;
    height: 100%;
}
.column3{
    width: 33%;
    float: right;
    height: 100%;
}
.img-profile-wrap {
    margin-top: 0.5%;
    left: 0;
    right: 0;
    margin-right: auto;
    width: 160px;
    height: auto;
    text-align: center;
    bottom: -50px;
    margin-left: auto;
    padding: 0 ;
}
.img-profile-wrap  p{
    font-family: shabnam;
    font-size: 16px;
    padding: 5px;
    margin-bottom: 10px;
}
.img-circle{
    border-radius: 50%;
    width: 160px;
    height: 160px;
    border: 1px solid #d9d9d9;
    background: #fff;
    padding: 28px;
    background-image: url("https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRyYukC_LcEZl_w6EJmMbv70WvmPZBdPFdwH-a_EsylSaOPPB77");
    background-position: center;
    background-size: cover;
}

.gender table{
    border: solid 1px  #d9d9d9;
    border-radius: 20px;
    width: 30%;
    margin-left: 140px;

}
.gender p{
    margin-top: 5px;
    text-align: center;
    color: blue;
}
.button{
    background-color:blue;
    border: blue solid 1px;
    border-radius: 20px;
    color: white;
    padding: 10px 80px;
    text-align: center;
    font-size: 16px;
    margin:0px auto;
    cursor: pointer;
    text-decoration: none;
}

</style>
