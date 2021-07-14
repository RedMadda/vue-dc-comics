<template>
  <header class="container">
    <a href="#"><img src="../assets/dc-logo.png" alt="Logo DC" /></a>
    <ul>
      <li
        v-for="(link, index) in Links"
        :key="index"
        :class="{ active: link.activated }"
      >
        <a href="#">{{ link.text }}</a>
      </li>
    </ul>
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

header {
  display: flex;
  justify-content: space-between;
  padding-top: 30px;
  img {
    width: 70px;
    height: 70px;
  }
  ul {
    display: flex;

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
</style>
