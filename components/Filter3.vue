<template>
  <div>
    <div class="filter-container">
      <h5>رنگ<div class="plus" id="color-plus" @click="clicked">+</div></h5>
    </div>
    <div class="colors" id="colors">
      <div v-for="c in colors" :key="c">
        <div class="color" :style="{backgroundColor: c}"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

  //props: ['brands'],

  data() {
    return {
      count : 1,
      colors: ['blue', 'white', 'black', 'yellow', 'blue', 'white', 'black', 'yellow', 'blue', 'white', 'black', 'yellow']
    }
  },

  methods: {

    clicked: function() {
      if(this.count%2==1)
        this.showColors();
      else
        this.hideColors();

      this.count++;
    },

    showColors: function() {
      document.getElementById("colors").style.display = "block";
      document.getElementById("color-plus").innerHTML = "-"
    },

    hideColors: function() {
      document.getElementById("colors").style.display = "none";
      document.getElementById("color-plus").innerHTML = "+"
    }
  }

}
</script>

<style scoped>
.filter-container {
  width: 250px;
  height: auto;
  background-color: #d7d7d7;
  text-align: right;
  color: #676767;
  padding: 10px;
  margin-top: 10px;
}

.plus {
  float: left;
  cursor: pointer;
}

.colors {
  display: none;
  width: 250px;
  height: 200px;
  overflow-y: scroll;
  background-color: #d7d7d7;
  color: #676767;
  position: relative;
}

.color {
  width: 35px;
  height: 35px;
  margin: 5px;
  border: solid 1px #676767;
  padding-right: 10px;
  float: right;
}

</style>
