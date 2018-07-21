<template>
  <div class="container">
    <div class="line">
      <div class="text">قیمت واحد</div>
      <div class="value">{{priceWithoutOff}}</div>
    </div>
    <div class="line">
      <div class="text" style="color:deeppink">تخفیف</div>
      <div class="value" style="color:deeppink">{{off}}</div>
    </div>
    <div class="empty"></div>
    <div class="line">
      <div class="text">قیمت نهایی</div>
      <div class="value">{{priceWithoutOff-off}}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['priceWithoutOff', 'off'],
}
</script>

<style scoped>
.container {
  margin-top: 5px;
  width: 100%;
  height: 100px;
}

.line {
  width: 100%;
  height: 20px;
}

.text {
  width: 50%;
  height: auto;
  float: right;
  text-align: right;
  color: #676767;
}

.value {
  width: 50%;
  height: auto;
  float: left;
  text-align: left;
  color: #676767;
}

.empty {
  width: 100%;
  height: 30px;
  border-bottom: solid 1px #676767;
}

</style>
