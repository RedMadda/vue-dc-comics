<template>
  <div id="bcc" class="main">
    <div class="container">
      <button class="btn-curr">current series</button>
      <div class="black-wrapper">
        <ComiCard 
        v-for="(comic, index) in NewSeries"
        :key="index"
        :book="comic"
        :srcCover="comic.thumb"
        :titleBook="comic.series"/>
      </div>
     <button class="up">upload now</button>
      <!-- banner available purchases, lightblue -->

      <ul class="products">
        <li v-for="(product, index) in Products" :key="index">
          <a href="#">
            <img :src="product.imgSrc" alt="Img">
           <span>{{product.text}}</span> 
          </a>
        </li>
      </ul>

    </div>
  </div>
</template>

<script>
import Products from "../dati/Products.js"
import ComiCard from "../components/ComiCard.vue"
import NewSeries from "../dati/ComicsAvail.js"
export default {
  data(){
    return {
      Products,
      NewSeries
    }
  },
  components: {
    ComiCard
  }
};
</script>

<style lang="scss" scoped>

@import "../style/var.scss";
@import "../style/mixins.scss";

#bcc {
  background: rgb(62,161,255);
  background: linear-gradient(0deg, rgba(62,161,255,1) 12%, rgba(0,0,0,1) 1%); 
  z-index:100;

  .container {
    width: 1040px;
    margin: auto;
    color: white;

    .btn-curr{
      @include btn(10px 15px, none);
      position:relative;
      top: -20px;
      left:0;
    }

    .black-wrapper{
      display:flex;
      width:100%;
      flex-wrap: wrap;
      justify-content: space-around;
      padding-top: 30px;
      padding-bottom: 50px;

    }
    .up{
      @include btn(15px 25px, none);
      position: relative;
      left:50%;
      transform: translateX(-50%);
      bottom: 70px;
    }
    .wrapper{
      height:80%;
    }

    ul{
      display: flex;
      justify-content: space-evenly;
      align-items: center;
      height: 100px;
      margin: 0;
    }

      li{
        list-style-type: none;
        display:flex;
        align-items: center;
        padding-right: 12px;

          a{
            text-decoration: none;
            color: white;
            display: flex;
            align-items: center;
            text-transform: $upText;
            font-size: 10px;

            img{
              height: 50px;
              padding-right: 10px;
            }
          }
      }
    }
}
</style>
