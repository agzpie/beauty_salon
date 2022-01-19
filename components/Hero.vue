<template>
    <div class="Hero container">
        <div class="text-container">
            <h1 class="header">Beauty Salon</h1>
            <p class="snippet">Book a visit at the best salon in town!</p>
            <button class="button btn">book here</button>
        </div>
    </div>  
</template>

<script>
export default {

}
</script>

<style scoped>
    .Hero {
        height: auto;
        width: 100%;
        position: relative;
        display: flex;
        flex-direction: column;
        padding: 10em 2em;
        align-items: flex-start;
        justify-content: center;
        
        background-image:#f5f2f0;background-image:  
        radial-gradient(at 67% 29%, #f5f2f0 0, transparent 52%),  
        radial-gradient(at 61% 57%, hsla(279,33%,67%,1) 0, transparent 40%),  
        radial-gradient(at 48% 46%, hsla(342,67%,73%,1) 0, transparent 56%);
        background-size: 400% 400%;
        animation: gradient 15s ease infinite;
       /* url(../assets/noise.png);
       #b38fc7
       #e88ca8
       527A66
       568C9C
       9C4E65

       */        
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
    .text-container {
        width: 80vw;
    }
    .header {
        font-family: 'Arima Madurai', Helvetica, sans-serif;
        font-size: 7em;
        font-weight: 100;
        color: #6B3646;
        mix-blend-mode:multiply;
    }
    .snippet {
        color: rgb(78, 59, 83);
        font-size: 1.25rem;
        font-family: 'Arima Madurai';
        font-weight: 300;
        mix-blend-mode:multiply;
        margin-bottom: 1em;
    }

    .button {
        padding: 1rem 3rem;
        margin-bottom: 4rem;
        font-weight: 500;
        width: 20rem;
        transition: 0.5s;
        mix-blend-mode:multiply;
    }
    .button:hover {
        width: 21.5rem;
        letter-spacing: 0.08em;
    }

    @media (max-width: 800px) {
        .Hero {
            height: 100vh;
            width: 100vw;
        }
        .header {
            font-size: 5em;
        }
    }
    @media (max-width: 565px) {
        .Hero {
            height: 100vh;
            width: 100vw;
            padding-top: 6rem;
        }
        .header {
            font-size: 4em;
            margin-bottom: 0.5em;
        }
        .button {
            width: 10rem;
            padding: 1rem 2rem;
        }
        .snippet {
            margin-top: 0rem;
        }
    }
</style>