<template>
  <section class="about-section">
    <div class="container-fluid d-flex justify-content-center align-items-center flex-column ">
      <div class="container row d-flex flex-column justify-content-center align-content-center">
        <div class="card text-center animate__animated animate__bounceIn">
          <div class="row g-0">
        <div class="col-lg-4 image-container">
          <img :src="$store.state.home[0].image" class="img-fluid hover-shadow about-image">
        </div>
        <div class="col-lg-8">
          <div class="card-body overflow-hidden">
            <h1 class="text-heading fw-semibold text-uppercase">About</h1>
            <h1 class="card-title display-4 animate__animated animate__fadeInRightBig animate__slow text-uppercase fw-bold">{{ $store.state.about[0].name }}</h1>
            <p class="card-text animate__animated animate__fadeInRightBig animate__slower">{{ $store.state.about[0].description }}</p>
            <p class="card-text">
            <a href="https://github.com/niyaazdaniels" target="_blank"><i class="fa-brands fa-github animate__animated animate__rotateIn animate__slower"></i></a>
          <a href="https://twitter.com/daniels_niyaaz" target="_blank"><i class="fa-brands fa-twitter animate__animated animate__rotateIn animate__slower "></i></a>
        <a href="https://www.linkedin.com/in/niyaaz-daniels-6694a7129/" target="_blank"><i class="fa-brands fa-linkedin animate__animated animate__rotateIn animate__slower "></i></a>
      </p>
       <a href="https://drive.google.com/uc?export=download&id=1VhXma-9eHWEU0Y9tS-DScq7nccc9UCsZ" class="button animate__animated animate__slideInUp animate__slower" target="_blank">
        <span class="button_lg">
         <span class="button_sl"></span>
          <span class="button_text hover-shadow">Download Resume</span>
          </span>
          </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
</section>
</template>

<script>
export default {
  components: {
  }
}
</script>

<style scoped>

.about-section{
  min-height: 100vh;
}

.card{
text-align: center;
padding: 30px;
background: #164A41;
color: #FFFFFF;
border: none;
border-radius: 0px;
box-shadow: 15px 12px 12px #164A41;
min-width: 90vw;
}
a {
  text-decoration: none;
}

p {
  font-size: 1rem;
}
.text-heading{
  color: #F1B24A;
}
.container-fluid{
  display: flex;
  justify-content: center;
  align-items: center;
  height: 90vh;
  min-width: 100vw;
  padding: 0;
}
i {
color: black;
padding: 15px;
border-radius: 15%;
margin-right: 10px;
margin-top: 10px ;
font-size: 1.3rem;

}
i:hover{
  transition: all .5s ease-in-out;
  box-shadow: 0px 0px 7px white;
  background: #F1B24A;
}
  .button {
  -moz-appearance: none;
  -webkit-appearance: none;
  appearance: none;
  border: none;
  background: none;
  color: #0f1923;
  cursor: pointer;
  position: relative;
  padding: 8px;
  margin-bottom: 20px;
  text-transform: uppercase;
  font-weight: bold;
  font-size: 14px;
  transition: all .15s ease;
}
.button_lg {
  position: relative;
  display: block;
  padding: 10px 20px;
  color: #fff;
  background-color: #0f1923;
  overflow: hidden;
  box-shadow: inset 0px 0px 0px 1px transparent;
}

.button_lg::before {
  content: '';
  display: block;
  position: absolute;
  top: 0;
  left: 0;
  width: 2px;
  height: 2px;
  background-color: #0f1923;
}

.button_lg::after {
  content: '';
  display: block;
  position: absolute;
  right: 0;
  bottom: 0;
  width: 4px;
  height: 4px;
  background-color: #0f1923;
  transition: all .2s ease;
}

.button_sl {
  display: block;
  position: absolute;
  top: 0;
  bottom: -1px;
  left: -8px;
  width: 0;
  background: #F1B24A;
  color: #000;
  transform: skew(-15deg);
  transition: all 1s ease;
}

.button_text {
  position: relative;
}

.button:hover {
  color: #0f1923;
}

.button:hover .button_sl {
  width: calc(100% + 15px);
}

.button:hover .button_lg::after {
  background-color: #fff;
}
h1 {
  border-right: solid 3px #164A41;
  white-space: nowrap;
  overflow: hidden;    
  color: rgba(255,255,255,.70);
}

/* Animation */
h1 {
  animation: animated-text 4s steps(60,end) 2s 1 normal both,
             animated-cursor 600ms steps(60,end) infinite;
}

/* text animation */

@keyframes animated-text{
  from{width: 0;}
  to{width: 55vw;}
}

/* cursor animations */

@keyframes animated-cursor{
  from{border-right-color: #F1B24A}
  to{border-right-color: transparent;}
}

@media (max-width: 2560px){
  .container{
    height: 35vh;
  }
}
@media (max-width: 1280px) {
.card {
  margin-top: 0px;
}
}
@media (max-width: 1024px) {
  img {
    height: 300px;
  }
  h1 {
    font-size: 20px;
  }
  p {
    font-size: 12px;
  }
 
  i {
    font-size: 15px;
    margin: 0;
  }
  .card-text {
    margin: 0;
  }
  
}
@media (max-width: 991px) {
 .card {
  position: relative;
  top: 5px;
 }
 .card-title {
  font-size: 2rem;
 }
 p {
  text-align: start;
 }
 .image-container {
  position: relative;
  display: flex;
  justify-content: start;
  padding: 20px;
 }
 h1 {
  position: relative;
  text-align: start;
 }
 
}
@media (max-width: 853px) {
  .about-image {
    height: 280px;
    border-radius: none;
  }
  p {
    font-weight: 300;
  }
}
@media (max-width: 679px){
  .about-image {
    height: 250px;
  }
  .card {
    font-size: 10px;
  }
  p {
    font-weight: 200;
  }

}
@media (max-width: 540px) {
  .about-image {
    height: 240px;
  }
  .card-title {
    font-size: 24px;
  }
  p {
    font-size: 10px;
  }
  i {
    font-size: 12px;
    margin: 0;
  }
  .card-body {
    padding: 5px;
  }
  /* .card-text {
    margin: 0;
  }
  .card {
    margin-bottom: 10px;
    margin-top: 80px;
  } */
}
@media (max-width: 430px) {
  .about-image{
    height: 230px;
  }
  p {
    font-size: 10px;
  }
  i {
    font-size: 12px;
  }
}
@media (max-width: 414px) {
  .about-image{ 
    height: 220px;
    padding: 0px;
  }
  .image-container{
    padding: 5px;
  }
  h1 {
    font-size: 18px !important;
  }
  p {
    font-size: 10px;
  }
  span.button_lg{
    font-size: 12px;
  }
  i {
    font-size: 12px;
  }
  .card{
    padding: 20px;
  }
  .card-text {
    margin: 0;
  }
}
@media (max-width: 375px){
.about-image {
  height: 200px;
}
h1 {
  font-size: 14px !important; 
}
p {
  font-size: 8px;
}
i {
  font-size: 10px;
}
span.button_lg {
  font-size: 8px;
}
.card-text {
  margin: 0;
}
}
@media (max-width: 360px){
  .card-text {
    margin: 0;
  }
}

@media (max-width: 320px) {
  .about-image {
    height: 180px;
  }
  .card-body p {
    font-size: 8px;
  }
  .card-body h1 {
    font-size: 15px;
  }
  .card-body i {
    font-size: 11px;
  }
  .card-body .button_text {
    font-size: 10px;
  }
  .text-heading {
    font-size: 10px;
    letter-spacing: 0px;
  }
}
@media (max-width: 280px) {
  p {
    font-size: 5px;
  }
}

</style>