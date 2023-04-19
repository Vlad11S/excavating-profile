<template>
  <div class="main">
    <div class="custom-header">
      <h1>Deyu groundwork and excavating</h1>
      <div class="menu">
        <p class="menu-item" @click="scrollToAbout">About</p>
        <p class="menu-item" @click="scrollToGallery">Gallery</p>
        <p class="menu-item" @click="scrollToReviews">Reviews</p>
      </div>
    </div>
    <div class="about" id="about">
      <div class="about-large">
        <div class="buttons">
          <div class="button" @click="showGr">
            Groundworking
          </div>
          <div class="button" @click="showEx">
            Excavating
          </div>
          <div class="button" @click="showFo">
            Foundations
          </div>
          <div class="button" @click="showLe">
            Leveling
          </div>
        </div>
        <div class="about-details" v-if="showGroundworking">
          <div class="about-text">
            Groundworking
          </div>
          <img src="../src/assets/background-excavator.jpg" alt="some image" class="about-image">
        </div>
        <div class="about-details" v-if="showExcavating">
          <div class="about-text">
            Excavating
          </div>
          <img src="../src/assets/background-excavator.jpg" alt="some image" class="about-image">
        </div>
        <div class="about-details" v-if="showFoundations">
          <div class="about-text">
            Foundations
          </div>
          <img src="../src/assets/background-excavator.jpg" alt="some image" class="about-image">
        </div>
        <div class="about-details" v-if="showLeveling">
          <div class="about-text">
            Leveling
          </div>
          <img src="../src/assets/background-excavator.jpg" alt="some image" class="about-image">
        </div>

      </div>
      <div class="about-small">
        <h2 class="location-header">Location</h2>
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d4885.857266232637!2d-0.8745583422735796!3d52.244679921232716!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1sro!2sro!4v1681852502083!5m2!1sro!2sro"
          width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"></iframe>
        <h2 class="contact-header">Contact information</h2>
        <div class="contact-info">
          <span class="social-span"><img src="../src/assets/phone.png" alt="phone" class="social-icons"> <a
              href="tel:07741302009">07741302009</a></span>
          <span class="social-span"><img src="../src/assets/facebook.png" alt="facebook" class="social-icons"><a
              href="https://www.facebook.com/profile.php?id=100090131125831">Andrei excavating</a></span>
        </div>
      </div>
    </div>
    <div class="gallery" id="gallery">
      <h1>Gallery</h1>
      <div class="carousel-container">
        <vueper-slides>
          <vueper-slide v-for="(slide, i) in slides" :key="slide.id" :image="slide.image" />
        </vueper-slides>
      </div>
    </div>
    <div class="reviews" id="reviews">
      <h1>Reviews</h1>
      <div class="stars">
        <img src="../src/assets/star.png" alt="star" class="star-image">
        <img src="../src/assets/star.png" alt="star" class="star-image">
        <img src="../src/assets/star.png" alt="star" class="star-image">
        <img src="../src/assets/star.png" alt="star" class="star-image">
      </div>
      <p class="review-text">
        Great excavations with the best technique!
      </p>
      <div class="stars">
        <img src="../src/assets/star.png" alt="star" class="star-image">
        <img src="../src/assets/star.png" alt="star" class="star-image">
        <img src="../src/assets/star.png" alt="star" class="star-image">
      </div>
      <p class="review-text">
        Great excavations with the best technique!
      </p>
      <div class="stars">
        <img src="../src/assets/star.png" alt="star" class="star-image">
        <img src="../src/assets/star.png" alt="star" class="star-image">
        <img src="../src/assets/star.png" alt="star" class="star-image">
        <img src="../src/assets/star.png" alt="star" class="star-image">
        <img src="../src/assets/star.png" alt="star" class="star-image">
      </div>
      <p class="review-text">
        Great excavations with the best technique!
      </p>
      <div class="stars">
        <img src="../src/assets/star.png" alt="star" class="star-image">
        <img src="../src/assets/star.png" alt="star" class="star-image">
        <img src="../src/assets/star.png" alt="star" class="star-image">
        <img src="../src/assets/star.png" alt="star" class="star-image">
      </div>
      <p class="review-text">
        Great excavations with the best technique!
      </p>
    </div>
  </div>
</template>

<style scoped>
.main {
  width: 100%;
  font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
  position: absolute;
  top: 0;
  left: 0;
}

.about {
  width: 100%;
  display: flex;
  margin-top: 210px;
}

.about-large {
  width: 65%;
  background-image: url('../src/assets/background-excavator.jpg');
  background-position: center;
  background-size: cover;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.about-small {
  width: 35%;
  background-color: #FFCB0F;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.location-header {
  transform: translateX(-200px);
}

.contact-header {
  transform: translateX(-140px);
}

iframe {
  width: 600px;
  height: 300px;
  margin-bottom: 20px;
  box-shadow: 5px 5px 50px 2px #000000;
}

.contact-info {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;
  transform: translateX(-145px);
  margin-bottom: 20px;
}

a {
  text-decoration: underline;
  color: black;
}

a:visited {
  text-decoration: underline;
  color: black;
}

.buttons {
  display: flex;
  width: 50%;
  justify-content: space-around;
  margin: 15px;
  transform: translateX(-200px);
}

.button {
  background-color: #FFCB0F;
  padding: 10px;
  box-shadow: 2px 2px 10px 1px #000000;
  border-radius: 10px;
  transition: all ease-in-out 0.4s;
  cursor: pointer;
}

.button:hover {
  font-weight: bold;
  transform: scale(1.02);
}

.about-details {
  width: 80%;
  background-color: whitesmoke;
  margin-bottom: 20px;
  margin-top: 10px;
  display: flex;
  border-radius: 10px;
  box-shadow: 5px 5px 50px 2px #000000;

}

.about-text {
  width: 800px;
  padding: 15px;
  margin-top: 20px;
}

.about-image {
  padding: 20px;
  max-width: 40%;
}

.custom-header {
  width: 100%;
  background-color: #FFCB0F;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-bottom: 20px;
  box-shadow: 5px 5px 50px 2px #000000;
  border-bottom: 1px solid black;
  position: fixed;
  top: 0;
  z-index: 999;
}

.menu {
  width: 300px;
  display: flex;
  justify-content: space-around;
}

.menu-item {
  font-size: 18px;
  transition: all ease-in-out 0.4s;
  cursor: pointer;
}

.menu-item:hover {
  text-decoration: underline;
}

.vueperslides__arrow {
  color: black
}

.carousel-img {
  width: 100%;
}

.gallery {
  width: 70%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 15%;
  margin-bottom: 30px;
}

.reviews {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.stars {
  display: flex;
  justify-content: space-around;
  width: 300px;
}

.star-image {
  width: 30px;
}

.review-text {
  font-size: 18px;
  margin-bottom: 40px;
  border-bottom: 1px solid black;
}

.social-icons {
  width: 30px;
  margin-right: 20px;
}

.social-span {
  display: flex;
  align-items: center;
  margin-bottom: 20px;
}
</style>
<script>
import { VueperSlides, VueperSlide } from 'vueperslides'
import 'vueperslides/dist/vueperslides.css'
export default {
  components: { VueperSlides, VueperSlide },
  data: () => ({
    slides: slides,
    showGroundworking: true,
    showExcavating: false,
    showFoundations: false,
    showLeveling: false
  }),
  methods: {
    showGr() {
      this.showGroundworking = true;
      this.showExcavating = false;
      this.showFoundations = false;
      this.showLeveling = false;
    },
    showEx() {
      this.showGroundworking = false;
      this.showExcavating = true;
      this.showFoundations = false;
      this.showLeveling = false;
    },
    showFo() {
      this.showGroundworking = false;
      this.showExcavating = false;
      this.showFoundations = true;
      this.showLeveling = false;
    },
    showLe() {
      this.showGroundworking = false;
      this.showExcavating = false;
      this.showFoundations = false;
      this.showLeveling = true;
    },
    scrollToAbout() {
      var element = document.getElementById('about');
      var headerOffset = 200;
      var elementPosition = element.getBoundingClientRect().top;
      var offsetPosition = elementPosition + window.pageYOffset - headerOffset;

      window.scrollTo({
        top: offsetPosition,
        behavior: "smooth"
      });
    },
    scrollToGallery() {
      var element = document.getElementById('gallery');
      var headerOffset = 150;
      var elementPosition = element.getBoundingClientRect().top;
      var offsetPosition = elementPosition + window.pageYOffset - headerOffset;

      window.scrollTo({
        top: offsetPosition,
        behavior: "smooth"
      });
    },
    scrollToReviews() {
      var element = document.getElementById('reviews');
      var headerOffset = 150;
      var elementPosition = element.getBoundingClientRect().top;
      var offsetPosition = elementPosition + window.pageYOffset - headerOffset;

      window.scrollTo({
        top: offsetPosition,
        behavior: "smooth"
      });
    }
  }
}
const slides = [
  {
    id: '1',
    title: 'Slide #1',
    content: 'Some image',
    image: '../src/assets/background-excavator.jpg'
  },
  {
    id: '2',
    title: 'Slide #2',
    content: 'Some image',
    image: '../src/assets/background-excavator.jpg'
  }
]
</script>
