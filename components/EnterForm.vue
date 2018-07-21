<template>
  <div class="form">
    <div class="img" @click="closeForm"></div><br/>
    <h6>ورود</h6>
    <p>شماره تماس یا ایمیل</p>
    <input type="text" class="inputText" placeholder="برای مثال rajabiseraji@outlook.com"/>
    <br/>
    <p>رمز عبور</p>
    <input type="text" class="inputText" value=""/>
    <p style="text-align:center; margin-right:0px">رمز عبور خود را فراموش کرده اید؟ <a href="###">کلیک کنید</a></p>
    <a href="/homePage"><input type="submit" class="btn" value="ورود"/></a>
    <br/>
  </div>
</template>

<script>
export default {
  methods: {
    closeForm: function() {
      document.getElementById("form1").style.display = "none"
    }
  }
}
</script>


<style scoped>
.img {
  width: 25px;
  height: 25px;
  float: right;
  padding: 2px;
  background-image: url("https://www.materialui.co/materialIcons/navigation/close_grey_192x192.png");
  background-size: cover;
  background-position: center;
  cursor: pointer;
}

.form {
  width: 300px;
  height: 310px;
  text-align: center;
  margin-left: auto;
  margin-right: auto;
  font-family:Shabnam;
  margin-top: 100px;
  border: solid 1px #808080;
  color: #676767;
}

p {
  font-size: 12px;
  color: #2223c8;
  text-align: right;
  margin-right: 20px;
}

.inputText {
  width: 83%;
  height: auto;
  font-size: 12px;
  background-color: #d7d7d7;
  color: #676767;
  border: solid 1px;
  border-color: #d7d7d7;
  border-radius: 20px;
  padding: 10px;
  text-align: left;
  direction: ltr;
  margin-bottom: 10px;
}

  p a {
    text-decoration:none;
  }

.btn {
  color:#ffffff;
  background-color:#676767;
  border:solid 1px #676767;
  border-radius:20px;
  margin-bottom:40px;
  text-decoration:none;
  padding:5px;
  padding-left:20px;
  padding-right:20px;
}

</style>

