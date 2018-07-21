<template>
  <div>
    <div class="filter-container">
      <h5>بر اساس برند<div class="plus" id="brand-plus" @click="clicked">+</div></h5>
      <input class="brandsearch" type="text" placeholder="جست و جو برند"/>
    </div>
    <div class="brands" id="brands">
      <div v-for="b in brands" :key="b">
        <div class="brand">
          <input type="checkbox">
          <span style="margin-right:5px;">{{b}}</span><br/>
        </div>
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
      brands: ['nick', 'addidas', 'apple', 'hi']
    }
  },

  methods: {

    clicked: function() {
      if(this.count%2==1)
        this.showBrands();
      else
        this.hideBrands();

      this.count++;
    },

    showBrands: function() {
      document.getElementById("brands").style.display = "block";
      document.getElementById("brand-plus").innerHTML = "-"
    },

    hideBrands: function() {
      document.getElementById("brands").style.display = "none";
      document.getElementById("brand-plus").innerHTML = "+"
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

.brands {
  display: none;
  width: 250px;
  height: 200px;
  overflow-y: scroll;
  background-color: #d7d7d7;
  color: #676767;
  position: relative;
}

.brandsearch {
  color: #676767;
  margin-right: 13px;
  direction: rtl;
}

.brand {
  width: 95%;
  height: auto;
  margin: 5px;
  border-bottom: solid 1px #676767;
  color: #878787;
  direction: rtl;
  text-align: right;
  padding-right: 10px;
}

</style>
