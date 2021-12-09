<template>
    <div class="Hero container">
        <div class="text-container">
            <h1 class="header">Beauty Salon</h1>
            <p class="snippet">Book a visit at the best salon in town!</p>
            <button class="button btn">book here</button>
        </div>
        <img src="~assets/blob.svg" alt="team picture" class="image">
    </div>  
</template>

<script>
export default {

}
</script>

<style scoped>
    .Hero {
        height: 80vh;
        max-width: 100vw;
        position: relative;
        display: flex;
        padding: 2em 1em;
        align-items: center;
        justify-content: space-between;
    }
    .text-container {
        width: 80vw;
    }
    .header {
        font-family: 'Arima Madurai', Helvetica, sans-serif;
        font-size: 5rem;
    }
    .snippet {
        color: grey;
        font-size: 1.25rem;
    }
    .image {
        position: absolute;
        max-height: 80vh;
        z-index: -1;
    }
    /*
    .overlay {
        background: rgba(0, 0, 0, 0);
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
    }*/
    .button {
        padding: 1rem 4rem;
        margin: 2rem 0rem 4rem 0rem;
        /*border-radius: 100rem;
        background-color: rgb(105, 93, 117);
        color: white;*/
        font-weight: 600;
        width: 20rem;
        transition: 0.5s;
    }
    .button:hover {
        width: 21.5rem;
        letter-spacing: 0.08em;
    }

    @media (max-width: 500px) {
        .Hero {
            height: 80vh;
            width: 100vw;
        }
    }
</style>