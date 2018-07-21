<template>
  <div>
    <div class="filter-container">
      <h5>دسته بندی ها<div class="plus" id="plus" @click="clicked">+</div></h5>
    </div>
    <div class="categories" id="categories">
      <ul style="list-style-type:square">
        <dt>مردانه</dt>
        <dd>ورزشی</dd>
        <dd>راحتی</dd>
        <dd>کتان</dd>
        <dt>زنانه</dt>
        <dd>ورزشی</dd>
        <dd>راحتی</dd>
        <dd>کتان</dd>
        <dt>بچگانه</dt>
        <dd>ورزشی</dd>
        <dd>راحتی</dd>
        <dd>کتان</dd>
      </ul>
    </div>
  </div>
</template>

<script>
export default {

  data() {
    return {
      count : 1
    }
  },

  methods: {

    clicked: function() {
      if(this.count%2==1)
        this.showCategories();
      else
        this.hideCategories();

      this.count++;
    },

    showCategories: function() {
      document.getElementById("categories").style.display = "block";
      document.getElementById("plus").innerHTML = "-"
    },

    hideCategories: function() {
      document.getElementById("categories").style.display = "none";
      document.getElementById("plus").innerHTML = "+"
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
}

.plus {
  float: left;
  cursor: pointer;
}

.categories {
  display: none;
  width: 250px;
  height: 200px;
  overflow-y: scroll;
  background-color: #d7d7d7;
  color: #676767;
  position: relative;
  text-align: right;
}

dt {
  margin-right: 20px;
}

dd {
  margin-right: 40px;
}
</style>
