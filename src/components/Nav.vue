<!-- 上部のナビゲーションバー !-->
<template>
  <div>
    <a href="#" class="nav-button" @click="clickSmoothScroll('#app')">TOP</a>
    <a href="#" class="nav-button" @click="clickSmoothScroll('#about')">ABOUT</a>
    <a href="#" class="nav-button" @click="clickSmoothScroll('#skill')">SKILL</a>
    <a href="#" class="nav-button" @click="clickSmoothScroll('#work')">WORKS</a>
    <a href="#" class="nav-button" @click="clickSmoothScroll('#contact')">CONTACT</a>
  </div>
</template>

<script>
// スムーズスクロール機能 //
export default {
  methods: {
    clickSmoothScroll (x) {
      event.preventDefault()
      this.$SmoothScroll(
        document.querySelector(x),
        800,//スクロール速度
        null,
        null,
        'y'
      )
    }
  }
}
</script>

<!-- CSS !-->
<style>
.nav-button {
  padding:10px;
  text-decoration: none;
  border-radius: 5px;
  margin-right:10px;
  margin-left: 10px;
  outline: none;
  color: rgb(83, 83, 83);
}


</style>
