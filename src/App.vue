<template>
  <div id="app">
    <div class="jumbo-container">
      <b-jumbotron header="Connor McRaven" lead="Custodial & Maintenance">
        <p>Contact Me: 715-497-2268 || connormcraven@gmail.com</p>
      </b-jumbotron>
    </div>
    <div class="body">
      <section class="section1 fade-in">
        <div class="image">
          <img class="imageSrc" src="./assets/logo.png" alt="logo">
        </div>
        <div class="text">
          <h2>About Me</h2>
          <hr>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis itaque provident est blanditiis commodi quo consectetur. Vitae, culpa nesciunt! Optio, eum quas ea et itaque repellat eligendi deleniti voluptas a!
        </div>
      </section>
      <section class="section2 fade-in">
        <div class="text">
          <h2>Rates and Availability</h2>
          <hr>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis itaque provident est blanditiis commodi quo consectetur. Vitae, culpa nesciunt! Optio, eum quas ea et itaque repellat eligendi deleniti voluptas a!
        </div>
        <div class="image">
          <img class="imageSrc" src="./assets/calendar.svg" alt="logo">
        </div>
      </section>
      <section class="section3 fade-in">
        <div class="image">
          <img class="imageSrc" src="./assets/logo.png" alt="logo">
        </div>
        <div class="text">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis itaque provident est blanditiis commodi quo consectetur. Vitae, culpa nesciunt! Optio, eum quas ea et itaque repellat eligendi deleniti voluptas a!
        </div>
      </section>
    </div>
    <Footer msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Footer
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300&display=swap');

#app {
  font-family: 'Poppins', sans-serif;
}

h2 {
  margin-bottom: 1rem;
}

.image {
  height: 20rem;
  width: 40vw;
  grid-area: imageArea;
  text-align: center;
}

.text {
  height: 20rem;
  width: 40vw;
  grid-area: textArea;
}

.jumbo-container {
  box-shadow: 0 4px 5px -2px rgba(0,0,0,.5);
}

.jumbotron {
  background-image: url("./assets/bg-1.jpg");
  background-size: cover;
  color: white;
  text-shadow: 2px 2px #1d1d1d;
}

section {
  padding: 3rem 0;
}

.imageSrc {
  height: 90%;
  width: auto;
}

.section1 {
  display: grid;
  grid-template-areas: 'imageArea textArea';
  justify-content: space-evenly;
  align-content: space-between;
  width: 100%;
}

.section2 {
  background-color: rgb(126, 240, 255);
  display: grid;
  grid-template-areas: 'textArea imageArea';
  justify-content: space-evenly;
  align-content: space-between;
  width: 100%;
}

.section3 {
  display: grid;
  grid-template-areas: 'imageArea textArea';
  justify-content: space-evenly;
  align-content: space-between;
  width: 100%;
}

</style>


// photos by: 
// <span>Photo by <a href="https://unsplash.com/@tomrumble?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Tom Rumble</a> on <a href="/s/photos/houses?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash</a></span>

// calendar
// <div>Icons made by <a href="http://www.freepik.com/" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div>