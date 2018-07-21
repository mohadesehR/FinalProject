<template>
  <div>
    <LogedInNavbar/>
    <BSImageSlider/>
    <div class="content">
      <CategoryCard catName = "مردانه" imgSrc = "https://file.digistyle.com/digistyle/Image/Webstore/Banner/1397/4/23/07a9ed68.jpg" url = "categories"/>
      <CategoryCard catName = "زنانه" imgSrc = "https://file.digistyle.com/digistyle/Image/Webstore/Banner/1397/4/23/ec90fa7b.jpg" url = "categories"/>
      <CategoryCard catName = "بچه گانه" imgSrc = "https://file.digistyle.com/digistyle/Image/Webstore/Banner/1397/4/23/28291bef.jpg" url = "categories"/>
      <p>بهترین ها را از ما خرید کنید</p>
      <div class="rightContent">
        <a href="###">تمام برندهای معتبر را با ما تجربه کنید</a>
      </div>
      <LeftContent/>
    </div>
    <Footer/>
  </div>
</template>

<script>
import LogedInNavbar from '@/components/LogedInNavbar'
import BSImageSlider from '@/components/BSImageSlider'
import CategoryCard from '@/components/CategoryCard'
import LeftContent from '@/components/LeftContent'
import Footer from '@/components/Footer'
export default {
  components : {
    LogedInNavbar,
    BSImageSlider,
    CategoryCard,
    LeftContent,
    Footer
  }
}
</script>

<style scoped>
.content {
  width: 1300px;
  height: 560px;
  margin-left: auto;
  margin-right: auto;
  margin-top: 10px;
}

p {
  text-align: center;
  font-size: 20px;
}

.rightContent {
    width:930px;
    border:solid 1px;
    border-color:#d7d7d7;
    text-align:center;
    padding:5px;
    float:right;
    height:290px;
    background-image:url("https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQGWvQvEiyraO8F43zEMcIxi93cggTez0IpAvrcEXtVKYZWgAuP");

}

.rightContent a {
  border:solid 1px;
    border-radius:20px;
    border-color:#2223c8;
    text-align:center;
    font-size:15px;
    float:right;
    width:250px;
    padding:5px;
    background-color:#2223c8;
    color:#fff;
    text-decoration:none;
    font-size:15px;
    margin-right:350px;
    margin-top:129px;
}
</style>

