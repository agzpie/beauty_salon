<template>
  <div class="container">
    <Navbar />
    <Hero />
    
    <Card 
      v-for="cardInfo in landingPageInfo"
      :key="cardInfo.id"
      :card="cardInfo"
    />
    <LargeCardDisplay 
      v-for="cardInfo in largeCardInfo"
      :key="cardInfo.id"
      :cardsSection="cardInfo"
    /> 
    <!--<Booking /> -->
    
  </div>  
</template>

<script>

import { largeCardSections } from "@/assets/data.js"
import { landingPageSections } from "@/assets/landingData.js"
export default {
  data() {
    return {
      largeCardInfo: largeCardSections,
      landingPageInfo: landingPageSections
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
}
.container {
  padding-left: 0;
  padding-right: 0;
  margin-left: 0;
  margin-right: 0rem;
  font-family: Roboto, sans-serif;
  font-weight: 100;
  max-width: 100vw;
  position: relative;
  align-items: center;
  justify-content: space-between;
  
}




</style>