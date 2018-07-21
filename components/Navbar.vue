<template>
    <div class ="header">
      <p>Clothster</p>
      <div class="itemPlaceHolder">
        <div class="register"><a>عضویت</a></div>
        <div class="login"><a @click="openForm">ورود</a></div>
        <SearchBox/>
      </div>
      <Menubar/>
    </div>
</template>

<script>
import EnterForm from '@/components/EnterForm'
import SearchBox from '@/components/SearchBox'
import Menubar from '@/components/Menubar'
export default {
  components : {
    SearchBox,
    Menubar
  },
  methodes : {
    openForm() {

    }
  }
}
</script>


<style scoped>
.header {
    margin-right:auto;
    margin-left:auto;
    width : 1140px;
    height : 120px;
}

    .header p {
        text-align:center;
        font-size:25px;
        color:#676767;
        margin-bottom:-15px;
    }

.register a {
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


    .register a:hover {
        border-color:#2223c8;
        color:#2223c8;
    }

    .register a:active {
        border-color:#2223c8;
        color:#2223c8;
    }

.login a {
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

    .login a:hover {
        border-color:#2223c8;
        background-color:#2223c8;
        color:#fff;
    }

    .login a:active {
        border-color:#2223c8;
        background-color:#2223c8;
        color:#fff;
    }

</style>

