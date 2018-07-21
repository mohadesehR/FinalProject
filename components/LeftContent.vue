<template>
  <div class="leftContent">
    <a href="###"><br /><div class="envelope-open"></div>
    <br />
    در خبرنامه ی ما <b><br />عضو شوید!</b>
    </a>
    <div class="empty"></div>
    <div class="getmail">
    <div class="envelope-close"></div>
    <input class="getbox" type="text" value="ایمیل خود را وارد کنید"/>
    </div>
    <div class="empty"></div>
    <div class="sendmail">
    <a href="###">عضو شوید</a>
    </div>
    </div>
</template>

<style scoped>
.leftContent {
    text-align:center;
    width:316px;
    margin-right:50px;
    border:solid 1px;
    border-color:#2223c8;
    background-color:#2223c8;
    color:#fff;
    padding:5px;
    float:right;
    height:290px;
}

.leftContent a {
    color:#fff;
    direction:rtl;
    text-decoration:none;
}

.envelope-open {
  width: 40px;
  height: 40px;
  background-image: url("https://cdn4.iconfinder.com/data/icons/ios7-active-2/512/Open_mail.png");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  margin-left: auto;
  margin-right: auto;
}

.envelope-close {
  width: 20px;
  height: 20px;
  float: right;
  background-image: url("http://www.newdesignfile.com/postpic/2014/02/email-message-icon_84361.png");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  margin-top: 2px;
}

.empty {
    height:20px;
}

.getmail {
    margin-top:20px;
    margin-left:auto;
    margin-right:auto;
    color:#2223c8;
    border:solid 1px;
    border-radius:20px;
    border-color:#2223c8;
    background-color:#fff;
    font-size:15px;
    width:180px;
    padding:5px;
    text-align:left;
}

.getbox {
    width:145px;
    text-align:right;
    font-size:13px;
    color:#2223c8;
    border:none;
}

    .getbox:hover {
        color:#676767;
    }

    .getbox:active {
        color:#676767;
    }

    .sendmail a {
        border:solid 1px;
        border-radius:20px;
        border-color:#000000;
        text-align:center;
        font-size:12px;
        width:80px;
        padding:10px;
        background-color:#000000;
        color:#fff;
        text-decoration:none;
    }

</style>
