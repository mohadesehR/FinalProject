<template>
  <div class="category">
    <div class="image" :style="{backgroundImage : 'url(' + imgSrc + ')'}"></div>
    <a :href=url>{{catName}}</a>
  </div>
</template>

<script>
export default {
  props: ['catName', 'imgSrc', 'url']
}
</script>


<style scoped>
.category {
  width: 433px;
  height: 200px;
  text-align: center;
  font-size: 20px;
  border: solid 1px #474747;
  float: right;
  margin-left: 0px;
  background-color: #878787;
  margin-bottom: 10px;
}

.category:hover {
  background-color: #2223c8;
}

.image {
  width: 100%;
  height: 165px;
  background-position: center;
  background-size: cover;
}

a {
  text-decoration: none;
  color: #ffffff;
  padding: 5px 20px;
}

</style>
