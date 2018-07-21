<template>
    <div class="input1">
      <p>{{title}}</p>
      <input class="textinput" type="text" :placeholder="defaultvalue"/>
    </div>
</template>

<script>
export default {
    props:['title', 'defaultvalue']
}
</script>

<style scoped>
.input1{
    position: relative;
    width:100% ;
    height: 22%;
    text-align: right;
    padding: 10px;
}

.input1  p{
    margin-right: 5%;
    color: blue;
    font-family: shabnam;
    font-size: 14px;
}

.textinput{
    position: relative;
    height: auto;
    margin-right: 5%;
    border:#d7d7d7 solid 1px;
    border-radius:20px;
    background-color: #d7d7d7;
    padding: 5px;
    width: 90%;
    direction: rtl;
}
.textinput  input {
  position: relative;
  width: 100%;
  height: 100%;
  border: none;
  background-color: dimgrey;
}
</style>
