<template>
    <div class="container">
        <h4 class="header">
            {{ cardsSection.title }}
        </h4>
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
    background-color: aqua;
    padding: 1rem;

        /*
    display: inline;
    display: grid;
    display: inline-grid;
    display: flow-root;
        align-items: center;
        justify-content: space-between;
        margin: 4rem 0 1rem 0;*/
    
}
    .header {
        font-weight: 700;
        font-size: 1.5rem;
    }
    .snippet {
        color: grey;
        margin-bottom: 1.5rem;
    }
    .cards-container {
        display: flex;
        justify-content: space-between;
    }
</style>