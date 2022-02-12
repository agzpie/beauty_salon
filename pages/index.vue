<template>
  <div class="container">
    <Hero />

    <div class="cards">
      <Card
        v-for="cardInfo in landingPageInfo"
        :key="cardInfo.id"
        :card="cardInfo"
      />
    </div>
    <LargeCardDisplay
      v-for="cardInfo in largeCardInfo"
      :key="cardInfo.id"
      :cards-section="cardInfo"
    />
  </div>
</template>

<script>
import { largeCardSections } from '@/assets/data.js'
import { landingPageSections } from '@/assets/landingData.js'
export default {
  data() {
    return {
      largeCardInfo: largeCardSections,
      landingPageInfo: landingPageSections,
    }
  },
}
</script>

<style>
.cards {
  border-top: 1px solid #6b3646;
}
</style>