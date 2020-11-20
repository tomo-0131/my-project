<template>
  <div class="header">
    <div class="header-inner">
      <h1 class="title">TOMOYUKI KUMAGAI</h1>
      <Nav class="nav"></Nav> <!--Nav.vueを読み込む !-->
    </div>
  </div>
</template>

<script>
import Nav from './Nav.vue' //ナビゲーションバーをコンポーネントを読み込む

export default {
  components: {
    Nav
  }
}
</script>

<style>
.header {
  background-color:#ffffff;
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 1;
}
.header-inner {
  margin-left: 5%;
  margin-right: 5%;
  display: flex;
}
.title {
  padding:20px 0px;
  margin:unset;
  color: rgb(83, 83, 83);
}
.nav {
  margin: auto ;
  margin-right: 0;
  padding: auto;
}
</style>
