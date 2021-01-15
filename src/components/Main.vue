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
              <li class="menuItems">
                <a href="">Dimas</a>
              </li>
              <b-nav-item href="#">Home</b-nav-item>
              <b-nav-item href="#" class="navActive">About</b-nav-item>
              <b-nav-item href="#">Education</b-nav-item>
              <b-nav-item href="#">Skills</b-nav-item>
              <b-nav-item href="#">Project</b-nav-item>
              <b-nav-item href="#">Contact</b-nav-item>
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
      <b-container>
        <b-row class="vh-100 text-center" align-v="center">
          <b-col xl="12">
            <b-img src="https://picsum.photos/200/200/?image=1025" rounded="circle" alt="Circle image" class="mb-4"></b-img>
            <h1 class="mb-4" style="color: black; font-weight: bold;">Dimas Prayoga</h1>
            <b-button class="main-navigation-button" variant="primary">Read More</b-button>
          </b-col>
        </b-row>
      </b-container>
    </section>
    <section id="about">
      <b-container>
        <b-row class="vh-100 text-center">
          <b-col xl="12">
            <h1 class="mb-4 mt-4">About Me</h1>
            <p>Junior Fullstack Developer</p>
          </b-col>
        </b-row>
      </b-container>
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
    document.getElementById('custom-navbar').style.padding = '25px 60px 10px 60px'
    document.getElementById('custom-navbar').classList.remove('navscroll')
  }
}
</script>

<style scoped>
@import '../assets/css/fonts.css';
* {font-family: medium;}

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
header .nav-item a:hover {
  color: white !Important;
}
header .nav-item:hover {
  border-radius: 10px;
  background-color: #292826 !important;
}
.menuItems, .menuItems a {
  color: black;
  text-decoration: none;
  padding: 5px;
}
.menuItems, .menuItems a:hover {
  background-color: black;
  color: white;
  padding: 5px;
  border-radius: 10px;
}
.navActive {
  background-color: #292826;
  border-radius: 10px;
}
.banner {
  min-height: 100vh;
  background-image: url(../assets/images/banner2.jpg);
  background-size: cover;
}
#about {
  background-color: #cecece;
}
</style>
