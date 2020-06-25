<template>
  <div id="app">
    <div class="jumbo-container">
      <b-jumbotron header="Connor McRaven" lead="Custodial & Maintenance">
        <p>Contact Me: 715-497-2268 || connormcraven@gmail.com</p>
      </b-jumbotron>
    </div>>
    <section class="section1 fade-in">
      <div class="image">
        <img class="imageSrc" src="./assets/logo.png" alt="logo">
      </div>
      <div class="text">
        <h2>About Me</h2>
        <hr>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis itaque provident est blanditiis commodi quo consectetur. Vitae, culpa nesciunt! Optio, eum quas ea et itaque repellat eligendi deleniti voluptas a!</p>
        <b-container class="lists-container">
          <b-row align-h="around">
            <b-col>
              <h5>Indoor</h5>
              <ul>
                <li class="about-li">Cleaning</li>
                <li class="about-li">Waste removal</li>
                <li class="about-li">Plumbing</li>
                <li class="about-li">Electrical</li>
                <li class="about-li">Appliance installation</li>
                <li class="about-li">Appliance removal</li>
                <li class="about-li">Much more!</li>
              </ul>
            </b-col>
            <b-col>
              <h5>Outdoor</h5>
              <ul>
                <li class="about-li">Mowing/edging</li>
                <li class="about-li">Weed removal</li>
                <li class="about-li">Powerwashing</li>
                <li class="about-li">Staining</li>
                <li class="about-li">Siding repair</li>
                <li class="about-li">Rain gutter cleaning</li>
                <li class="about-li">Much more!</li>
              </ul>
            </b-col>
          </b-row>
        </b-container>
      </div>
    </section>
    <section class="section2 fade-in">
      <div class="section2-div">
        <div class="text">
          <h2>Rates and Availability</h2>
          <hr>
          <ul>
            <li class="rates-li">Potential availability is 7 days a week - Monday through Sunday!</li>
            <li class="rates-li">Flat-rate of $22.50/hour</li>
            <li class="rates-li">No extra charge for Saturday/Sunday</li>
            <li class="rates-li">Free Estimates</li>
          </ul>
          <h4 style="margin-top: 3rem;">Please call or email with any questions!</h4>
        </div>
        <div class="image">
          <img class="imageSrc" src="./assets/calendar.svg" alt="logo">
        </div>
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
  overflow-x: hidden;
  font-size: 20px;
}

ul {
  padding-left: 18px !important;
}

.rates-li {
  margin-top: 1rem;
}

.about-li {
  margin-top: .5rem;
}

h2 {
  margin-bottom: 1rem;
}

/* h5 {
  text-align: center;
}

about-lists-div {
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  
}

.inner-list-div {
  max-width: 30%;
}  */

.imageSrc {
  height: 90%;
  width: auto;
}

.image {
  height: 20rem;
  width: 40vw;
  max-width: 500px;
  grid-area: imageArea;
  text-align: center;
  margin: auto;
  display: flex;
  align-items: center;
  justify-content: center;
}

.text {
  /* height: 20rem; */
  width: 40vw;
  max-width: 500px;
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
  margin-bottom: 0;
}

.lists-container {
  padding: 0;
}

section {
  padding: 4rem 0;
}

.section1 {
  display: grid;
  grid-template-areas: 'imageArea textArea';
  justify-content: space-evenly;
  align-content: center;
  width: 100%;
  max-width: 1600px;
  margin: auto;
  /* height: 30rem; */
}

.section2 {
  background-color: rgb(126, 240, 255);
  width: 100vw;
}

.section2-div {
  display: grid;
  grid-template-areas: 'textArea imageArea';
  justify-content: space-evenly;
  align-content: space-between;
  max-width: 1600px;
  margin-left: auto;
  margin-right: auto;
}

.section3 {
  display: grid;
  grid-template-areas: 'imageArea textArea';
  justify-content: space-evenly;
  align-content: space-between;
  width: 100%;
  max-width: 1600px;
  margin: auto;
}

</style>


// photos by: 
// <span>Photo by <a href="https://unsplash.com/@tomrumble?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Tom Rumble</a> on <a href="/s/photos/houses?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash</a></span>

// calendar
// <div>Icons made by <a href="http://www.freepik.com/" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div>