<template>
  <div class="container">
    <div class="about-hero">
        <h1 class="about-header">About us</h1>
        <img src="~/assets/images/team.jpg" alt="some image" class="team" />
        <img src="~/assets/images/divider.svg" alt="some image" class="divider" />
        <p class="about-snippet"><strong>Meet the team: </strong>Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt.<br><strong>Neque porro quisquam est</strong>, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem. Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur? <br><strong>Quis autem vel </strong> iure reprehenderit qui in ea voluptate velit esse quam nihil molestiae consequatur, vel illum qui dolorem eum fugiat quo voluptas nulla pariatur?</p>
    </div>

    <div class="cards">
      <Card 
        v-for="cardInfo in aboutPageInfo"
        :key="cardInfo.id"
        :card="cardInfo"
      />
    </div>
  </div>  
</template>

<script>
import { aboutPageSections } from "@/assets/landingData.js"
export default {
  data() {
    return {
      aboutPageInfo: aboutPageSections
    }
  }
} 
</script>

<style>
html {
  height: 100%;
}
body {
  min-height: 100%;
  background-color: #f5f2f0;
  margin-left: 0%;
  margin-right: 0%;
}
.container {
  padding-left: 0%;
  padding-right: 0%;
  font-family: Roboto, sans-serif;
  font-weight: 100;
  min-width: 100%;
  position: relative;
  align-items: center;
  justify-content: space-between;
}
.about-hero {
    min-height: 100vh;
    width: 100%;
    position: relative;
    display: flex;
    flex-direction: column;
    padding: 2rem;
    padding-top: 10rem;
    align-items: center;
    background-image:#f5f2f0;background-image:  
    radial-gradient(at 67% 29%, #f5f2f0 0, transparent 52%),  
    radial-gradient(at 61% 57%, hsla(279,33%,67%,1) 0, transparent 40%),  
    radial-gradient(at 48% 46%, hsla(342,67%,73%,1) 0, transparent 56%);
    background-size: 400% 400%;
    animation: gradient 15s ease infinite;      
}
@keyframes gradient {
    0% {
    background-position: 0% 50%;
    }
    50% {
        background-position: 100% 50%;
    }
    100% {
        background-position: 0% 50%;
    }
}
.about-header {
    font-family: 'Arima Madurai', Helvetica, sans-serif;
    font-size: 7em;
    font-weight: 100;
    color: #6B3646;
    mix-blend-mode:multiply;
    margin-top: -5rem; 
    position: absolute;
} 
.team {
    margin: auto;
    width: 60%;
    border: 1px solid #6B3646;
}
.divider {
    width: 30%;
    margin-top: 2rem;
}
.about-snippet {
    color: rgb(78, 59, 83);
    font-size: 1.05rem;
    font-family: 'Arima Madurai';
    font-weight: 300;
    mix-blend-mode:multiply;
    margin: 2rem;
    width: 80%;
}
.cards {
  border-top: 1px solid #6B3646;
}

@media (max-width: 800px) {
    .Hero {
        min-height: 100vh;
        width: 100vw;
    }
    .header {
        font-size: 5em;
    }
}
@media (max-width: 565px) {
    .Hero {
        min-height: 100vh;
        width: 100vw;
        padding-top: 6rem;
    }
    .header {
        font-size: 4em;
        margin-bottom: 0.5em;
    }
    .snippet {
        margin-top: 0rem;
    }
}
</style>