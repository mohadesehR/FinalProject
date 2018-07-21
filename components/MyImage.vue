<template>
  <div class="myImage">
    <img src={{imageSrc}}/>
  </div>
</template>

<script>
export default {
  props: ["imageSrc", "imgeIndex"]
}
</script>

<style scoped>

.myImage {
  width: 1300px;
  height: 92%;
  margin-right: auto;
  margin-left: auto;
  border: solid 1px #676766;
  margin-top: 10px;
}

img {
  width: 100%;
  height: 100%;
}

</style>

