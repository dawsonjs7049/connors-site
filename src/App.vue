<template>
  <div id="app">
    <div class="jumbo-container">
      <b-jumbotron header="Connor McRaven" lead="Custodial & Maintenance">
        <p class="mt-4">Contact Me: 715-497-2268 || connormcraven@gmail.com</p>
      </b-jumbotron>
    </div>
    <section class="section1 fade-in">
      <div class="image">
        <img class="imageSrc animate" src="./assets/logo.png" alt="logo">
      </div>
      <div class="text">
        <h2>About Me</h2>
        <hr>
        <p>My name is Connor McRaven and I offer many different household services to help you keep up with day to day maintenance or with the remodeling you've been dreaming of. I come from a background of service work and have the experience to see your job done right. My availability and services are listed below, please don't hesitate to call with any questions!</p>
        <hr>
        <b-container class="lists-container">
          <b-row align-h="around">
            <b-col cols="12" sm="6">
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
            <b-col cols="12" sm="6">
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
            <li class="rates-li">Accept work in a 50 mile radius of Eau Claire, WI</li>
            <li class="rates-li">Free Estimates</li>
          </ul>
          <h4 style="margin-top: 3rem;">Please call or email with any questions!</h4>
        </div>
        <div class="image">
          <img class="imageSrc animate" src="./assets/calendar.svg" alt="logo">
        </div>
      </div>
    </section>

    <section class="section3 fade-in">
      <!-- <div class="image">
        <img class="imageSrc" src="./assets/logo.png" alt="logo">
      </div>
      <div class="text">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis itaque provident est blanditiis commodi quo consectetur. Vitae, culpa nesciunt! Optio, eum quas ea et itaque repellat eligendi deleniti voluptas a!
      </div> -->
      <h2 style="text-align: center;">Previous Work</h2>
      <hr class="mb-5">
      <b-container>
        <b-row align-h="around">
          <b-col cols="12" md="6" lg="3">
            <div>
              <b-carousel
                id="carousel-1"
                :interval="3000"
                controls
                indicators
                img-width="500"
                img-height="900"
                fade
              >
                <b-carousel-slide img-src="./assets/vinyl-before.png" alt="picture"></b-carousel-slide>
                <b-carousel-slide img-src="./assets/vinyl-after.png"></b-carousel-slide>
              </b-carousel>
            </div>
          </b-col>
          <b-col cols="12" md="6" lg="3">
            <div>
              <b-carousel
                id="carousel-1"
                :interval="3000"
                controls
                indicators
                img-width="500"
                img-height="900"
                fade
              >
                <b-carousel-slide img-src="./assets/vinyl-before.png" alt="picture"></b-carousel-slide>
                <b-carousel-slide img-src="./assets/vinyl-after.png"></b-carousel-slide>
              </b-carousel>
            </div>
          </b-col>
          <b-col cols="12" md="6" lg="3">
            <div>
              <b-carousel
                id="carousel-1"
                :interval="3000"
                controls
                indicators
                img-width="500"
                img-height="900"
                fade
              >
                <b-carousel-slide img-src="./assets/vinyl-before.png" alt="picture"></b-carousel-slide>
                <b-carousel-slide img-src="./assets/vinyl-after.png"></b-carousel-slide>
              </b-carousel>
            </div>
          </b-col>
          <b-col cols="12" md="6" lg="3">
            <div>
              <b-carousel
                id="carousel-1"
                :interval="3000"
                controls
                indicators
                img-width="500"
                img-height="900"
                fade
              >
                <b-carousel-slide img-src="./assets/vinyl-before.png" alt="picture"></b-carousel-slide>
                <b-carousel-slide img-src="./assets/vinyl-after.png"></b-carousel-slide>
              </b-carousel>
            </div>
          </b-col>
        </b-row>
      </b-container>


    </section>
    <Footer msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import Footer from './components/Footer.vue';
import { onMounted, onUnmounted } from "@vue/composition-api";
export default {
  setup () {
    //this setup function is used to build the fade-in effects
    var fadeInElements = []
    var fadedElements = []

    onMounted(() => {
      //get the three sections to fade-in
      fadeInElements = Array.from(document.getElementsByClassName('fade-in'))

      //when the user scrolls, call the handleScroll method
      document.addEventListener('scroll', handleScroll)

      //call function once when page first loads
      handleScroll()
    })

    onUnmounted(() => {
      document.removeEventListener('scroll', handleScroll)
    })

    const handleScroll = () => {
      //cycle through each section, if its visible (by more than 200px), set opacity to 1 and scale up, then remove that section from the array
      let loop1 = fadeInElements
      console.log("FADE IN ELEMENTS: " + fadeInElements)
      console.log("LOOP1: " + loop1)
      for (var i = 0; i < loop1.length; i++) {
        var elem = loop1[i]
        
        if (isElemVisible(elem)) {
          elem.style.opacity = '1'
          elem.style.transform = 'scale(1)'
          // console.log(fadeInElements.splice(i, 1)[0].className.substring(0, 8)) // only allow it to run once
          fadedElements = [...fadedElements, loop1.splice(i, 1)]
          
        } 
      }

      //  console.log("FADED ELEMENTS: " + fadedElements)
      // for (var j = 0; j < fadedElements.length; j++) {
      //     let elem = fadedElements[j];
      //     if(!isElemVisibleAtAll(elem)) {
      //       elem.style.opacity = '0';
      //       elem.style.transform = 'scale(.8)'

      //       fadedElements.splice(j, 1);
      //     }
        
      // }
    }

    const isElemVisible = (el) => {
      var rect = el.getBoundingClientRect()
      var elemTop = rect.top + 200 // 200 = buffer
      var elemBottom = rect.bottom
      return elemTop < window.innerHeight && elemBottom >= 0
    }

    // const isElemVisibleAtAll = (el) => {
    //  var rect = el.getBoundingClientRect()
    //   var elemTop = rect.top // 200 = buffer
    //   var elemBottom = rect.bottom
    //   return elemTop < window.innerHeight && elemBottom >= 0
    // }
  },
  name: 'App',
  components: {
    Footer
  },
  data() {
    return {
      
    }
  },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300&display=swap');

#app {
  font-family: 'Poppins', sans-serif;
  overflow: hidden;
  font-size: 20px;
}

ul {
  padding-left: 18px !important;
}

h5 {
   font-weight: bold;
}


section:hover > div > img {
  animation: bounce 1s infinite alternate;
}

section:hover > div > div > img {
  animation: bounce 1s infinite alternate;
}

@keyframes bounce {
  from {
    transform: translateY(0px);
  }
  to {
    transform: translateY(-15px);
  }
}
@-webkit-keyframes bounce {
  from {
    transform: translateY(0px);
  }
  to {
    transform: translateY(-15px);
  }
}

.rates-li {
  margin-top: 1rem;
}

#prev-tag {
  margin-bottom: 2rem;
  text-align: center;
}

.about-li {
  margin-top: .5rem;
}

.fade-in {
  opacity: 0;
  transition: 0.3s all ease-out;
  transform: scale(0.8);
  box-sizing: border-box;
}

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
  text-shadow: 2px 2px #0c0c0c;
  margin-bottom: 0;
}

.carousel {
  margin-bottom: 2rem;
  border-radius: 5px;
  overflow: hidden;
  box-shadow: 5px 5px #c0a6a6;
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
  width: 100%;
  max-width: 1600px;
  margin: auto;
}

@media only screen and (max-width: 800px) {
  .section2-div {
    grid-template-areas: 'imageArea'
                         'textArea';
    justify-content: space-evenly;
    align-content: space-between;
    max-width: 1600px;
    margin-left: auto;
    margin-right: auto;
  }

  .section1 {
    grid-template-areas: 'imageArea'
                         'textArea';
    justify-content: space-evenly;
    align-content: center;
    width: 100%;
    max-width: 1600px;
    margin: auto;
  }

  .image {
    margin-bottom: 4rem;
  }

  h2 {
    text-align: center;
  }

  h5 {
    margin-top: 2rem;
  }

  .text {
    width: 75vw;
    max-width: 75vw;
  }

  .image {
    width: 75vw;
    max-width: 75vw;
  }
}


</style>


// photos by: 
// <span>Photo by <a href="https://unsplash.com/@tomrumble?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Tom Rumble</a> on <a href="/s/photos/houses?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash</a></span>

// calendar
// <div>Icons made by <a href="http://www.freepik.com/" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div>

//start command is 'npm run serve'