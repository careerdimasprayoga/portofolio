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
              <b-nav-item href="#" class="mr-3">Education</b-nav-item>
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
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Facere quidem amet libero, molestiae quas ea quos eos deleniti reiciendis nemo velit repellat maiores porro obcaecati vel eius, nulla inventore. Blanditiis. Lorem ipsum dolor sit amet consectetur adipisicing elit. Consectetur ea, amet modi quam maiores perferendis sapiente labore sint exercitationem alias illo beatae ipsa quidem officia accusamus velit animi est praesentium.</p>
          </b-col>
        </b-row>
      </b-container>
    </section>
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

.parallax {
  background-image: url(../assets/images/banner2.jpg);
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
/* header .nav-item a:hover {
  color: white !Important;
} */
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
.banner {
  min-height: 100vh;
}
#about {
  background-color: rgb(248, 248, 248);
}
</style>
