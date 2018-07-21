<template>
  <div class="container">
    <table class="addrTable">
      <tr class="tr1">
        <td width=5% rowspan="2" style="text-align:center"><input type="radio" name="addressTable" checked="checked"></td>
        <td class="td1" width=30%>تحویل گیرنده: {{name}}</td>
        <td class="td1" width=40%>شماره تلفن ثابت: {{phone}}</td>
        <td class="td1" width=25%>شماره تلفن همراه: {{mobile}}</td>
        <td class="td1" width=5%><div class="img"></div></td>
      </tr>
      <tr class="tr2">
        <td class="td1" colspan="2">آدرس: {{address}}</td>
        <td class="td1">کدپستی: {{postID}}</td>
        <td class="td1"><div class="img2"></div></td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  props: ['id','name', 'phone', 'mobile', 'address', 'postID'],
}
</script>

<style scoped>
.container {
  width: 80%;
  height: auto;
  margin-left: auto;
  margin-right: auto;
}

.addrTable {
  text-align: right;
  direction: rtl;
  color: #676767;
  border: solid 2px #676767;
  border-collapse: collapse;
  width: 100%;
  margin: 10px 0px;
}

.tr1 {
  border-bottom: solid 1px #676767;
}

td {
  padding: 10px;
}

.td1 {
  border-right: solid 1px #676767;
}

.addrTable:hover {
  border-color: blue;
}

.img {
  width: 35px;
  height: 30px;
  background-size: cover;
  background-position: center;
  background-image: url("https://cdn4.iconfinder.com/data/icons/design-4/100/14-512.png");
}

.img2 {
  width: 35px;
  height: 35px;
  background-size: cover;
  background-position: center;
  background-image: url("https://www.materialui.co/materialIcons/navigation/close_grey_192x192.png");
}

</style>
