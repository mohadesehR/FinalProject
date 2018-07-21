<template>
  <div>
    <LogedInNavbar/>
    <div class="content" id="content">
      <ProductRightContent :images="images" :image="image" :off="off"/>
      <ProductLeftContent :images="images" :brand="brand" :name="name" :priceWithOff="priceWithOff"
      :priceWithoutOff="priceWithoutOff" :color="color" :sizes="sizes" :properties="properties"/>
    </div>
    <ProductBottomContent/>
    <ItemSlider title="محصولات مرتبط" :productCards="this.productCards" id="slider"/>
    <Footer/>
  </div>
</template>

<script>
import LogedInNavbar from '@/components/LogedInNavbar'
import ProductRightContent from '@/components/ProductRightContent'
import ProductLeftContent from '@/components/ProductLeftContent'
import ProductBottomContent from '@/components/ProductBottomContent'
import ItemSlider from '@/components/ItemSlider'
import Footer from '@/components/Footer'
export default {

  props: [
    'id'
  ],

  data() {
    return {
      images: [
        {
          src: "https://file.digistyle.com/digistyle/Image/Webstore/Product/P_11793/350/Girls-Straight-Pants.JPG"
        },
        {
          src: "https://file.digistyle.com/digistyle/Image/Webstore/Product/P_9241/350/Girls-Cotton-Leggings-5d72ec.JPG"
        },
        {
          src: "https://file.digistyle.com/digistyle/Image/Webstore/Product/P_14476/350/Girls-Plain-Legging-7322c0.jpg"
        },
        {
          src: "https://file.digistyle.com/digistyle/Image/Webstore/Product/P_11660/350/GIRL-KNITTED-TROUSERS.JPG"
        },
        {
          src: "https://file.digistyle.com/digistyle/Image/Webstore/Product/P_11659/350/GIRL-WOVEN-TROUSERS.jpg"
        }
      ],
      image: {src:"https://file.digistyle.com/digistyle/Image/Webstore/Product/P_11659/350/GIRL-WOVEN-TROUSERS.jpg"},
      off: "20%",
      brand: "nike",
      name: "کفش ",
      priceWithOff: "80.000",
      priceWithoutOff: "100.000",
      color: "مشکی",
      sizes: ["38", "40", "42", "44", "46", "48", "50", "52", "54"],
      properties: ["hi", "well", "yes", "good", "No", "ok", "cancel", "bad", "weak"],
      productCards: [
        {
          id: "1",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "2",
          image: "https://file.digistyle.com/digistyle/Image/Webstore/Product/P_113461/350/Men-Cotton-Liner-Socks-Pack-of-3-cf639b.jpg",
          brand: "nick",
          name: "جوارب",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "3",
          image: "https://file.digistyle.com/digistyle/Image/Webstore/Product/P_131110/350/Men-Cotton-Liner-Socks-Pack-of-3-ffc363.jpg",
          brand: "addidas",
          name: "جوراب مردانه",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "4",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "5",
          image: "https://file.digistyle.com/digistyle/Image/Webstore/Product/P_122331/350/Men-Leg-Warmer-665469.jpg",
          brand: "adiddas",
          name: "شلوار راحتی",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "6",
          image: "https://file.digistyle.com/digistyle/Image/Webstore/Product/P_133273/350/Men-Short-Sleeve-T-Shirts-ec17a2.JPG",
          brand: "coka",
          name: "تیشرت",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "7",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "8",
          image: "https://file.digistyle.com/digistyle/Image/Webstore/Product/P_133274/350/Men-Plain-Shorts-a9b0a5.JPG",
          brand: "addidas",
          name: "شلوارک",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "9",
          image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "کفش",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        },
        {
          id: "10",
          image: "https://file.digistyle.com/digistyle/Image/Webstore/Product/P_131965/350/Men-Straight-Chinos-08afa7.jpghttps://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQv6XL7abFE_jmrsIQISuOq1djt_kFI9Cs3U5X4hURVTT2REo3-PQ",
          brand: "nick",
          name: "شلوار کتان",
          off: "20%",
          priceWithOff: "80.000",
          priceWithoutOff: "100.000"
        }
      ],
    }
  },

  components: {
    LogedInNavbar,
    ProductRightContent,
    ProductLeftContent,
    ProductBottomContent,
    ItemSlider,
    Footer
  }
}
</script>

<style scoped>
.content {
  margin-top: 100px;
  width: 1080px;
  height:800px;
  margin-left: auto;
  margin-right: auto;
}

</style>

