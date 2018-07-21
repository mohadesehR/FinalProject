<template>
  <div id="document">
    <nuxt/>
    <div class ="header">
      <p>Clothster</p>
      <div class="itemPlaceHolder">
        <div class="register"><div class="a1" @click="openForm2">عضویت</div></div>
        <div class="login"><div class="a2" @click="openForm1">ورود</div></div>
        <SearchBox/>
      </div>
      <Menubar/>
    </div>
    <div class="content">
      <div class="myForm" id="form1">
        <EnterForm/>
      </div>
      <div class="myForm" id="form2">
        <RegisterForm/>
      </div>
    </div>
    <Footer/>
  </div>
</template>

<script>
import SearchBox from '@/components/SearchBox'
import Menubar from '@/components/Menubar'
import EnterForm from '@/components/EnterForm'
import RegisterForm from '@/components/RegisterForm'
import Footer from '@/components/Footer'
export default {
  components : {
    SearchBox,
    Menubar,
    EnterForm,
    RegisterForm,
    Footer,
    },

    methods: {
      openForm1: function() {
        var element = document.getElementById("form2");
        element.style.display = "none";
        document.getElementById("form1").style.display = "block";
      },
      openForm2: function() {
        var element = document.getElementById("form1");
        element.style.display = "none";
        document.getElementById("form2").style.display = "block"
      }
    },
}
</script>

<style scoped>
.content {
  width: 1140px;
  height: 500px;
  margin-left: auto;
  margin-right: auto;
}

.myForm {
  display: none;
  width: 100%;
  height: 100%;
}

.header {
    margin-right:auto;
    margin-left:auto;
    width : 1140px;
    height : 60px;
}

    .header p {
        text-align:center;
        font-size:25px;
        color:#676767;
        margin-bottom:-15px;
    }

.a1 {
    border:solid 1px;
    border-color:#676767;
    border-radius:20px;
    text-align:center;
    font-size:15px;
    float:right;
    width:70px;
    padding:5px;
    color:#676767;
    text-decoration:none;
    padding-top: 0px;
}

.itemPlaceHolder{
  height:35px;
}


    .a1:hover {
        border-color:#2223c8;
        color:#2223c8;
        cursor: pointer;
    }

    .a1:active {
        border-color:#2223c8;
        color:#2223c8;
    }

.a2 {
    border:solid 1px;
    border-radius:20px;
    border-color:#676767;
    text-align:center;
    font-size:15px;
    float:right;
    width:70px;
    padding:5px;
    background-color:#676767;
    margin-right:2px;
    color:#fff;
    text-decoration:none;
    padding-top: 0px;
}

    .a2:hover {
        border-color:#2223c8;
        background-color:#2223c8;
        color:#fff;
        cursor: pointer;
    }

    .a2:active {
        border-color:#2223c8;
        background-color:#2223c8;
        color:#fff;
    }
</style>
