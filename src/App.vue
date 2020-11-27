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
        <font-awesome-icon icon="user-circle" class="nav-icon"/>
        <p class="comment">ABOUT</p>
      </a>
      <a href="#" class="link-content" @click="clickSmoothScroll('#skill')">
        <font-awesome-icon icon="code" class="nav-icon"/>
        <p class="comment">SKILL</p>
      </a>
      <a href="#" class="link-content" @click="clickSmoothScroll('#works')">
        <font-awesome-icon icon="hammer" class="nav-icon"/>
        <p class="comment">WORKS</p>
      </a>
      <a href="#" class="link-content" @click="clickSmoothScroll('#contact')">
        <font-awesome-icon icon="handshake" class="nav-icon"/>
        <p class="comment">CONTACT</p>
      </a>
    </div>

    <div id="top">
      <div id="main">
      <vue-typer :text="['Hello.\n\n Thank You For Visiting !']" class="top-text" :repeat='0'
      :preTypeDelay="1000" :typeDelay="120" :preEraseDelay="5000" :eraseDelay="2000"></vue-typer>
      </div>
      <vue-particles
        :particleOpacity="0.7"
        linesColor="#dedede"
        :particlesNumber="100"
        :shapeType="circle"
        :particleSize="6"
        :linesWidth="2"
        :lineLinked="true"
        :lineOpacity="0.4"
        :linesDistance="150"
        :moveSpeed="4"
        :hoverEffect="true"
        :hoverMode="grab"
        :clickEffect="true"
        :clickMode="push"
        :retina_detect="true"
      >
      </vue-particles>
    </div>

    <About id="about"></About>
    <Skill id="skill"></Skill>
    <Works id="works"></Works>
    <Contact id="contact"></Contact>
    <div class="page_top">
      <a href="#" v-scroll-to="'body'">
        TOP
      </a>
    </div>
    <Footer></Footer>
  </div>
</template>

<script>

import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import About from './components/About.vue'
import Skill from './components/Skill.vue'
import Works from './components/Works.vue'
import Contact from './components/Contact.vue'

import 'normalize.css'

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    About,
    Skill,
    Works,
    Contact
  },
  methods: {
    clickSmoothScroll (x) {
      event.preventDefault()
      this.$SmoothScroll(
        document.querySelector(x),
        800,
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
  color: #333;
}

#top{
  color: rgb(41, 41, 41);
  position: relative;
  background-image: url(./assets/bg.jpg);
  background-color:#ffffff;
  background-size: cover;
  height: 80%;
}

#main{
  position: absolute;
  top: 30%;
  left: 50%;
  transform: translateY(-50%) translateX(-50%);
  color:rgb(255, 255, 255)
}

.particles{
  z-index: 1;
  height: 80vh;
  color: #333;
  top: 0;
  left: 0;
  width: 80%;
  height: 70%;

}

.top-texts {
  z-index: 10;
  color: #ffffff;
}

.res{
  display: none;
  font-size: 30px;
}

.res-title{
  padding: 10px;
  margin: 0;
  color: rgb(66, 66, 66);
}

.vue-typer .custom.char{
  color: rgb(255, 255, 255);
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
  color: rgb(39, 14, 14);
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
  .nav-res {
    display: none;
    color: rgb(82, 5, 88);
  }
  #main {
    font-size: 1110px;
  }
  .top-text {
    font-size: 100px;
  }
}

@media screen and (max-width: 768px){

  #top{
    color: rgb(41, 41, 41);
    position: relative;
    background-image: url(./assets/bg.jpg);
    background-color:#ffffff;
    background-size: cover;
  }

  .vue-typer .custom.char{
    color: rgb(129, 0, 0);
    font-size: 10px;
  }

  .top-text {
    font-size: 10px;
    color: aqua;
  }

  #header{
    display: none;
  }

  .res{
    display: contents;
    background-color: #ffffff;
    font-size: 40px;
  }

  .res-title{
    background-color: #ffffff;
    font-size: 60px;
  }

  .nav-res{
  position: sticky;
  position: -webkit-sticky;
  top: 0;
  z-index: 1;
  background-color: #ffffff;
  margin-top: 45px;
  padding-bottom: 10px;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-around;
}

  .content-title{
    margin-bottom: 30px;
    font-size: 30px;
  }
}

@media screen and (max-width: 480px) {
  #top{
    color: rgb(255, 255, 255);
    position: relative;
    background-image: url(./assets/bg.jpg);
    background-color:#696969;
    background-size: cover;
  }

  #main {
    margin-top: -1670px;
  }

  .top-text{
    font-size: 21px;
  }

  .vue-typer .custom.char{
  color: rgb(255, 255, 255);
  font-size: 12px;
  }

  .res {
    font-size: 25px;
    font-weight: 700;
  }
}
</style>
