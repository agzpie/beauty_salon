<template>
  <div class="container">
    <Navbar />
    <Hero />
    
    <!-- -->

    
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


<style scoped>
.container {
  margin: 2rem 0 2rem 0;
}


</style>