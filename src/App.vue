<template>
  <div id="app">
    <Header id="header"></Header>
    <div class="res"><h1 class="res-title"></h1>TOMOYUKI KUMAGAI</div>
    <div class="nav-res">
      <a href="#" class="link-content" @click="clickSmoothScroll('#app')">
        <font-awesome-icon icon="image" class="nav-icon"/>
        <p class="comment">TOP</p>
      </a>
      <a href="#" class="link-content" @click="clickSmoothScroll('#about')">
        <font-awesome-icon icon="user-ciecle" class="nav-icon"/>
        <p class="comment">ABOUT</p>
      </a>
      <a href="#" class="link-content" @click="clickSmoothScroll('#skill')">
        <font-awesome-icon icon="code" class="nav-icon"/>
        <p class="comment">SKILL</p>
      </a>
      <a href="#" class="link-content" @click="clickSmoothScroll('#work')">
        <font-awesome-icon icon="hammer" class="nav-icon"/>
        <p class="comment">WORKS</p>
      </a>
      <a href="#" class="link-content" @click="clickSmoothScroll('#contact')">
        <font-awesome-icon icon="handshake" class="nav-icon"/>
        <p class="comment">CONTACT</p>
      </a>
    </div>
    <About id="about"></About>
    <Skill id="skill"></Skill>
    <Work id="work"></Work>
    <Contact id="contact"></Contact>

    <Footer></Footer>
  </div>
</template>

<script>

import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import About from './components/About.vue'
import Skill from './components/Skill.vue'
import Work from './components/Work.vue'
import Contact from './components/Contact.vue'

import 'normalize.css'

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    About,
    Skill,
    Work,
    Contact
  },
  methods: {
    clickSmoothScroll (x) {
      event.preventDefault()
      this.$SmoothScroll(
        document.querySelector(x),
        600,
        null,
        null,
        'y'
      )
    }
  }
}
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Comic+Neue:ital,wght@1,300&display=swap");

#app{
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  text-align: center;
}

#top{
  position: relative;
  /*background-image: url(./assets/yoru2.jpg);*/
  background-color:#03111a;
  background-size: cover;
  height: 100vh;
}

#main{
  position: absolute;
  top: 30%;
  left: 50%;
  transform: translateY(-50%) translateX(-50%);
}

.particles{
  z-index: 1;
  height: 100vh;
}

.res{
  display: none;
}

.res-title{
  padding: 10px;
  margin: 0;
  color: rgb(83, 83, 83);
}

.vue-typer .custom.char{
  color: aliceblue;
}

.nav-res{
  display: none;
}

.nav-icon{
  font-size: 1.5em;
}

.comment{
  margin:5px 0;
  font-weight: 500;
  color: rgb(83, 83, 83);
}

.link-content{
  color: rgb(83, 83, 83);
  text-decoration: none;
  min-width: 8%;
  font-size: 10px;
  text-align: center;
}
.top-text{
  color: rgb(83, 83, 83);
  font-size: 50px;
}
.icon{
  font-size: 0.8em;
}
.text{
    font-weight: 500;
}
.content-title {
  padding: 40px 0 10px 0;
  margin: 50px 20% 100px 20%;
  position: relative;
  font-size: 2em;
  color: #333;
  border-bottom: rgba(12, 50, 78, 0.4) 3px solid;
}

@media screen and (max-width: 1200px) {
  .top-text{
    font-size: 35px;
  }
}

@media screen and (max-width: 768px){
  .top-text{
    font-size: 25px;
  }
  #header{
    display: none;
  }
  .res{
    display: contents;
    background-color: #03111a;
  }
  .nav-res{
  position: sticky;
  position: -webkit-sticky;
  top: 0;
  z-index: 1;
  background-color: #03111a;
  padding: 10px;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-around;
}

.content-title{
  margin-bottom: 30px;
}
}

@media screen and (max-width: 450px) {
  .top-text{
    font-size: 11px;
  }
}
</style>
