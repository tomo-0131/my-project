<template>
  <div class="contact">
    <h1 class="content-title"><font-awesome-icon icon="handshake" class="icon"/> CONTACT </h1>
    <div>
        <img src="../assets/Contact us.gif" alt="logo" class="skills-image">
    </div>
      <div class="link">
        <a href="https://twitter.com/tk_engineers" class="link-icon"><font-awesome-icon :icon="['fab','twitter']" class="web-icon twitter"/></a>
        <a href="mailto:tmyk.engineer@gmail.com" class="link-icon"><font-awesome-icon icon="envelope" class="web-icon mail"/></a>
        <a href="http://github.com/tomo-0131" class="link-icon"><font-awesome-icon :icon="['fab','github']" class="web-icon github"/></a>
        <a href="https://myportfolio425.web.app/" class="link-icon"><font-awesome-icon icon="blog" class="web-icon hateblo"/></a>
      </div>
  </div>
</template>

<style>
.sam{
    text-align: center;
}
.link{
    display:inline-flex;
    width: 30%;
    justify-content: center;
}
.link-icon{
    margin: 0 10px;
    margin-bottom: 20px;
}
.web-icon{
    font-size: 2em;
    background-color: white;
    padding:0.3em;
    border-radius: 50%;
}
.web-icon:hover{
    color: white;
}
.twitter{
    color: #1DA1F2;
}
.twitter:hover{
    background-color: #1DA1F2;
}
.mail{
    color: #DD5144;
}
.mail:hover{
    background-color: #DD5144;
}
.github{
    color: #171515;
}
.github:hover{
    background-color: #171515;
}
.hateblo{
    color: #193278;
}
.hateblo:hover{
    background-color: #193278;
}
@media screen and (max-width: 768px){
    .contact {
        margin-top: -130px;
    }
    .content-title {
        margin-top: -300px;
    }
    .web-icon{
        color:white;
    }
    .twitter{
        background-color: #1DA1F2;
    }
    .mail{
        background-color: #DD5144;
    }
    .github{
        background-color: #171515;
    }
    .hateblo{
        background-color: #193278;
    }
}
</style>
