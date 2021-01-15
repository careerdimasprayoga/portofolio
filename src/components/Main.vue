<template>
  <div>
    <header>
      <b-navbar toggleable="lg" id="custom-navbar">
        <b-navbar-brand href="#">Dimas Prayoga</b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
            <b-navbar-nav>
              <b-nav-item href="#banner" class="mr-3">Home</b-nav-item>
              <b-nav-item href="#about" class="mr-3 active">About</b-nav-item>
              <b-nav-item href="#" class="mr-3">Skills</b-nav-item>
              <b-nav-item href="#" class="mr-3">Project</b-nav-item>
              <b-nav-item href="#" class="mr-3">Contact</b-nav-item>
            </b-navbar-nav>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
      <!--  -->
      <!-- <b-navbar type="dark" variant="transparent" id="custom-navbar">
        <b-navbar-nav class="ml-5">
          <b-nav-item href="#banner" class="mr-3">Home</b-nav-item>
          <b-nav-item href="#about" class="mr-3">About Me</b-nav-item>
          <b-nav-item href="#" class="mr-3 navActive">Services</b-nav-item>
          <b-nav-item href="#" class="mr-3">Skills</b-nav-item>
          <b-nav-item href="#" class="mr-3">Projects</b-nav-item>
          <b-nav-item href="#" class="mr-3">Contact</b-nav-item>
        </b-navbar-nav>
      </b-navbar> -->
    </header>
    <section class="banner" id="banner">
      <div class="parallax">
        <b-container>
          <b-row class="vh-100 text-center" align-v="center">
            <b-col xl="12">
              <b-img src="https://picsum.photos/200/200/?image=1025" rounded="circle" alt="Circle image" class="mb-4"></b-img>
              <h1 class="mb-4" style="color: black; font-weight: bold;">Dimas Prayoga</h1>
              <b-button class="main-navigation-button" variant="primary">Read More</b-button>
            </b-col>
          </b-row>
        </b-container>
      </div>
    </section>
    <section id="about">
      <b-container>
        <b-row class="text-center" align-v="center" style="height: 300px;">
          <b-col xl="10" offset="1">
            <h3 class="mb-4">About Me</h3>
            <p>I am Fullstack Developer Javascript. I love create new system that help, usefull and easier people. Lorem ipsum dolor sit amet consectetur adipisicing elit. Odio temporibus corporis tenetur rem est quas quisquam id dolore ex quo incidunt expedita numquam ratione amet sunt nemo, tempora cum eos. Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium omnis repellat quaerat beatae totam expedita, ad nihil perspiciatis odit nulla sequi soluta ratione recusandae possimus at quis earum magnam eos?</p>
          </b-col>
        </b-row>
      </b-container>
    </section>
    <section class="skills" id="skills">
      <div class="parallax2">
        <b-container>
          <b-row class="vh-100 text-center" align-v="center">
            <b-col xl="12">
              <div class="asem" style="width: 100%; height: 600px; background-color: white; border-radius: 10px;">
                <h3>Skills</h3>
              </div>
            </b-col>
          </b-row>
        </b-container>
      </div>
    </section>
  </div>
</template>

<script>
window.onscroll = function () {
  navScrollFunction()
}
function navScrollFunction () {
  if (document.body.scrollTop > 80 || document.documentElement.scrollTop > 80) {
    document.getElementById('custom-navbar').style.padding = '10px 60px 10px 60px'
    document.getElementById('custom-navbar').classList.add('navscroll')
  } else {
    document.getElementById('custom-navbar').style.padding = '20px 60px 10px 60px'
    document.getElementById('custom-navbar').classList.remove('navscroll')
  }
}
</script>

<style scoped>
@import '../assets/css/fonts.css';
* {font-family: medium;}

.parallax {
  background-image: url(../assets/images/banner2.jpg);
  height: 100%;
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.parallax2 {
  background-image: url(../assets/images/banner.jpg);
  height: 100%;
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
header #custom-navbar {
  position: fixed;
  width: 100%;
  z-index: 1;
  padding: 10px 60px 10px 60px;
}
.navscroll {
  background-color: #ffffff !important;
}
header .nav-item a{
  color: black !important;
}
header .nav-item:hover {
  border-radius: 15px;
  background-color: #292826 !important;
}
.active {
  background-color: #292826;
  border-radius: 15px;
}
.navbar-nav > .active > a {
  color: white !important;
}
.nav-item > a:hover {
  color: white !important;
}
.banner, .skills {
  min-height: 100vh;
}
#about {
  background-color: rgb(248, 248, 248);
}
</style>
