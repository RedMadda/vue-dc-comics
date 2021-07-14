<template>
  <div id="bcc">
    <div class="container">
      <div class="wrapper">
      <h2>Contents goes here</h2>
      <h2>Contents goes here</h2>
      <h2>Contents goes here</h2>
      <h2>Contents goes here</h2>
      <h2>Contents goes here</h2>
      <h2>Contents goes here</h2>
      <h2>Contents goes here</h2>
      <h2>Contents goes here</h2>
      <h2>Contents goes here</h2>
   </div>
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
export default {
  data(){
    return {
      Products
    }
  }
};
</script>

<style lang="scss" scoped>

@import "../style/var.scss";
#bcc {
  background: rgb(62,161,255);
  background: linear-gradient(0deg, rgba(62,161,255,1) 20%, rgba(0,0,0,1) 10%); 
  z-index:100;
  .container {
    width: 1040px;
    margin: auto;
    color: white;
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
