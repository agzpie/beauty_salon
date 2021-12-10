<template>
    <div class="container">
        <h2 class="header">
            {{ cardsSection.title }}
        </h2>
        <p class="snippet">
            {{ cardsSection.snippet }}
        </p>
        <div class="cards-container">
            <LargeCard 
                v-for="card in cardsSection.cards"
                :key="card.id"
                :card="card"
            />
        </div>
    </div>
</template>

<script>
    export default {
        props: ['cardsSection']
    }
</script>

<style scoped>
.container {
    margin: 3rem 0 1rem 0;
    padding: 1rem;    
}
    .header {
        font-size: 2rem;
        font-family: 'Arima Madurai';
        font-weight: 300;
    }
    .snippet {
        font-family: Roboto;
        font-weight: 300;
        color: rgb(39, 38, 38);
        margin-bottom: 1.5rem;
    }
    .cards-container {
        display: flex;
        justify-content: space-between;
    }
</style>