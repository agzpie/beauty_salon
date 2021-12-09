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
.container {
  padding-left: 0;
  padding-right: 0;
  margin-left: 0;
  margin-right: 0rem;
  font-family: Roboto, sans-serif;
  font-weight: 100;
  background-color: rgb(136, 212, 212);
  max-width: 100vw;
  position: relative;
  align-items: center;
  justify-content: space-between;
    
}


</style>