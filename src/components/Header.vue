<template>
  <header>
    <!-- nav -->
    <div class="container">
      <a href="#"><img src="../assets/dc-logo.png" alt="Logo DC" /></a>
      <ul>
        <li
          v-for="(link, index) in Links"
          :key="index"
          :class="{ active: link.activated }">
        <a href="#">{{ link.text }}</a>
        </li>
      </ul>
    </div>
    <!-- jumbo -->
    <div class="jumbo">
      <img :src="require('../assets/jumbotron.jpg')" alt="jumbo bkc">
    </div>
  </header>
</template>

<script>
import Links from "../dati/Links.js";
export default {
  data() {
    return {
      Links
    };
  },
};
</script>

<style lang="scss" scoped>

@import "../style/var.scss";

.container {
  height: 80px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  
  img {
    width: 60px;
    height: 60px;
  }
  ul {
    display: flex;
    height: 100%;
    line-height: 60px;

    li {
      list-style-type: none;
      padding: 10px;
      text-transform: $upText;

      &:hover {
        background-color: rgb(112, 174, 236);
      }
      &.active {
        border-bottom: 5px solid rgb(56, 144, 233);
      }

      a {
        text-decoration: none;
        color: #353535;
      }
    }
  }
}

.jumbo{
  width: 100%;
  height: 350px;
  overflow: hidden;
  
  img{
    width: inherit;
  }
}
</style>
