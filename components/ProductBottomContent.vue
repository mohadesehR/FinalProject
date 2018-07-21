<template>
  <div class="container">
    <div class="headLine">
      <div class="tab" style="margin-right:40%" @click="showTable">مشخصات محصول</div>
      <div class="tab" @click="showComments">نظرات کاربران</div>
    </div>
    <table id="tbl">
      <tr v-for="p in prop" :key="p.title">
        <td>{{p.title}}</td>
        <td>{{p.value}}</td>
      </tr>
    </table>
    <div id="comments">
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      prop: [
        {
          title: "مشخصه",
          value: "مقدار مشخصه"
        },
        {
          title: "مشخصه",
          value: "مقدار مشخصه"
        },
        {
          title: "مشخصه",
          value: "مقدار مشخصه"
        },
        {
          title: "مشخصه",
          value: "مقدار مشخصه"
        },
      ]
    }
  },

  methods: {
    showTable: function() {
      document.getElementById("comments").style.display = "none";
      document.getElementById("tbl").style.display = "inline-table";
    },

    showComments: function() {
      document.getElementById("tbl").style.display = "none";
      document.getElementById("comments").style.display = "block";
    }

  }
}
</script>

<style scoped>
.container {
  width: 100%;
  height: auto;
}

.headLine {
  width: 100%;
  height: 50px;
  background-color: rgb(184, 222, 247);
}

.tab {
  padding: 10px;
  float: right;
  cursor: pointer;
}

.tab:active {
  text-decoration: underline;
}

table {
  width: 100%;
  text-align: right;
  direction: rtl;
  display: inline-table;
}

tr {
  width: 100%;
}

tr:nth-child(even) {
  background-color: rgb(214, 238, 253);
}

td {
  padding: 10px 10px;
}

#comments {
  width: 100%;
  display: none;
  height: 200px;
}

</style>
