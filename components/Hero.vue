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
        max-width: 100%;
        position: relative;
        display: flex;
        padding: 0 1em;
        align-items: center;
        justify-content: space-between;
    }
    .text-container {
        width: 50%;
    }
    .header {
        font-family: Helvetica, Arial, sans-serif;
        font-size: 5rem;
    }
    .snippet {
        color: grey;
        font-size: 1.25rem;
    }
    .image {
        position: absolute;
        max-height: 80vh;
        margin-top: 0rem;
        margin-right: 0vw;
        z-index: -1;
    }
    .overlay {
        background: rgba(0, 0, 0, 0);
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
    }
    .button {
        margin: 2rem 0rem 4rem 0rem;
        padding: 1rem 4rem;
        border-radius: 100rem;
        background-color: rgb(105, 93, 117);
        color: white;
        width: 20rem;
        font-weight: 700;
        transition: 0.5s;
    }
    .button:hover {
        width: 21.5rem;
    }

    @media (max-width: 500px) {
        .Hero {
            height: 80vh;
        }
    }
</style>