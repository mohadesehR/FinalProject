<template>
  <div>
    <Category
      :brands="this.brandCards"
      :populareProducts="this.productCards"
      :newProducts="this.productCards"
      bnr1 = "https://file.digistyle.com/digistyle/image/webstore/banner/1397/2/22/d496613e_set1.jpg"
      bnr2 = "https://file.digistyle.com/digistyle/image/webstore/banner/1397/3/27/df50bd93_set1.jpg"/>
  </div>
</template>

<script>
import Category from '@/components/Category'
export default {
  components : {
    Category
  },

  data() {
    return {
      brandCards: [
        {
          image: "https://file.digistyle.com/digistyle/Image/Webstore/Banner/1397/2/18/6c0c5222.jpg",
          name: "ecco",
          url: ""
        },
        {
          image: "https://file.digistyle.com/digistyle/Image/Webstore/Banner/1397/3/30/a55ab0dd.jpg",
          name: "MANGO",
          url: ""
        },
        {
          image: "https://file.digistyle.com/digistyle/Image/Webstore/Banner/1397/2/18/11486225.jpg",
          name: "addidas",
          url: ""
        },
        {
          image: "https://file.digistyle.com/digistyle/Image/Webstore/Banner/1397/2/25/52292ee7.jpg",
          name: "DEBENHAMS",
          url: ""
        },
        {
          image: "https://file.digistyle.com/digistyle/Image/Webstore/Banner/1397/2/25/c3936c7f.jpg",
          name: "JACKJONES",
          url: ""
        },
        {
          image: "https://file.digistyle.com/digistyle/Image/Webstore/Banner/1397/2/25/1aebd5fe.jpg",
          name: "SELECTED",
          url: ""
        },
    ],
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
  }
}
</script>

