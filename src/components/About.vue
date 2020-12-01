<template>
  <div>
    <h1 class="content-title"><font-awesome-icon icon="user-circle" class="icon" /> ABOUT</h1>
    <div>
      <div>
        <img src="../assets/about.svg" alt="logo" class="about-image">
      </div>
      <div class="about">
        <div class="me">
          <h2><font-awesome-icon icon="pen" class="icon" /> NAME</h2>
          <p class="text">Tomoyuki Kumagai</p>
        </div>

        <div class="me">
          <h2><font-awesome-icon icon="school" class="icon" /> UNIVERSITY</h2>
          <p class="text">Nanzan Univ.</p>
        </div>

        <div class="me">
          <h2><font-awesome-icon icon="birthday-cake" class="icon" /> BIRTH DAY</h2>
          <p class="text">1989/04/25</p>
        </div>

        <div class="me">
          <h2><font-awesome-icon icon="search" class="icon" /> INTEREST</h2>
          <p class="text">Vue.js, Ruby on Rails, AWS</p>
        </div>
      </div>
    </div>
  </div>
</template>


<style>
.about {
  display:inline-flex;
  padding-left: 5%;
  padding-right: 5%;
}

.me{
    margin:0 50px;
}

.about-image {
   height: 300px;
   margin-top: -70px;
}

@media screen and (max-width: 768px){
	.about {
		flex-direction: column;
	}
	.me {
    margin: 0 auto;
	}
  .about-image {
   height: 300px;
   margin-top: -10px;
  }
}

</style>
