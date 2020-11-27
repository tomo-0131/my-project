<template>
  <div>
    <h1 class="content-title"><font-awesome-icon icon="code" class="icon"/> Skill</h1>
    <div>
      <div class="languages">
        <h3 class="lang-text">開発で使用した言語等</h3>
        <div class="lang">
          <img src="../assets/lang/html-5.svg" alt="logo" class="lang-image">
          <h3 class="lang-comment">HTML</h3>
        </div>
        <div class="lang">
          <img src="../assets/lang/css-3.svg" alt="logo" class="lang-image">
          <h3 class="lang-comment">CSS</h3>
        </div>
        <div class="lang">
          <img src="../assets/lang/javascript.svg" alt="logo" class="lang-image">
          <h3 class="lang-comment">JavaScript</h3>
        </div>
        <div class="lang">
          <img src="../assets/lang/ruby.svg" alt="logo" class="lang-image">
          <h3 class="lang-comment">Ruby</h3>
        </div>
        <div class="lang">
          <img src="../assets/lang/rails.svg" alt="logo" class="lang-image">
          <h3 class="lang-comment">RubyOnRails</h3>
        </div>
        <div class="lang">
          <img src="../assets/lang/react.svg" alt="logo" class="lang-image">
          <h3 class="lang-comment">REACT</h3>
        </div>
        <div class="lang">
          <img src="../assets/lang/vue.svg" alt="logo" class="lang-image">
          <h3 class="lang-comment">Vue.js</h3>
        </div>
        <div class="lang">
          <img src="../assets/lang/aws.svg" alt="logo" class="lang-image">
          <h3 class="lang-comment">AWS</h3>
        </div>
        <div class="lang">
          <img src="../assets/lang/docker-icon.svg" alt="logo" class="lang-image">
          <h3 class="lang-comment">Docker</h3>
        </div>
        <div class="lang">
          <img src="../assets/lang/circleci.svg" alt="logo" class="lang-image">
          <h3 class="lang-comment">CircleCI</h3>
        </div>
        <div class="lang">
          <img src="../assets/lang/git.svg" alt="logo" class="lang-image">
          <h3 class="lang-comment">GIT</h3>
        </div>
        <div class="lang">
          <img src="../assets/lang/github-icon.svg" alt="logo" class="lang-image">
          <h3 class="lang-comment">GitHub</h3>
        </div>
        <div class="lang">
          <img src="../assets/lang/visual-studio-code.svg" alt="logo" class="lang-image">
          <h3 class="lang-comment">VScode</h3>
        </div>
        <div class="lang">
          <img src="../assets/lang/slack-icon.svg" alt="logo" class="lang-image">
          <h3 class="lang-comment">Slack</h3>
        </div>
        <div class="lang">
          <img src="../assets/lang/macOS.svg" alt="logo" class="lang-image">
          <h3 class="lang-comment">macOS</h3>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.languages{
    text-align: center;
    padding-left: 15%;
    padding-right: 15%;
}
.lang{
    margin :10px 30px;
    display: inline-block;
    width: 100px;
}
.lang-comment{
  width: 100px;
}
.lang-image{
  height: 50px;
  width: 50px;
}

.lang-text {
  margin-top: -10px;
}

@media screen and (max-width: 768px) {
  .languages{
      padding-left: 15%;
      padding-right: 15%;
  }
  .lang{
      margin :10px 30px;
      display: inline-flex;
      width: 100px;
  }
  .lang-comment{
    width: 100px;
  }
  .lang-image{
    height: 50px;
    width: 50px;
  }

  .lang-text {
    margin-top: -10px;
  }
}

</style>
