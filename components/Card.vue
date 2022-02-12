<template>
    
        <kinesis-container event="scroll" class="flex-container">            
            <div class="image-container">
                <kinesis-element :strength="100" type="translate" axis="y">
                    <b-img :src="require(`@/assets/images/${ card.image || 'image_1.jpg'}`)" fluid alt="some image" class="image"></b-img>
                </kinesis-element>
            </div>
            <div class="headers">
                <kinesis-element :strength="-150" type="translate" axis="y">
                    <h1 class="header1"> {{ card.title }} </h1>
                </kinesis-element>

                <kinesis-element :strength="-250" type="depth_inv" axis="y">  
                    <h1 class="header2"> {{ card.title }} </h1>
                </kinesis-element>
            </div>
            
            <div class="card-content">
                <p class="card-snippet"> {{ card.snippet }} </p>
                <div class="btn">
                    <OutlineButton> {{ card.button }} </OutlineButton>
                </div>
            </div>

        </kinesis-container>

</template>

<script>
import { KinesisContainer, KinesisElement } from 'vue-kinesis';
export default {
    props: [ 'card' ],

    components: {
        KinesisContainer,
        KinesisElement
    },
}
</script>

<style>
.flex-container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-evenly;
    margin: 0rem;
    width: 100%;
    border-bottom: 1px solid #6B3646;
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
.image-container {
    width: 50%;
    height: 80%;
    overflow: hidden;
    align-content: center;
    justify-content: center;
}
.image {
    margin: 0;
    border-right: 1px solid #6B3646;    
    object-fit: cover;
}
.headers {
    z-index: 5;
    position: absolute;
    top: 5rem;
    left: 0;
}
.header1 {
    margin: -3rem 0 -2rem 1rem;
    color: rgba(146, 100, 129, 0.582);
    font-family: 'Arima Madurai';
    font-weight: 100;
    font-size: 4rem;
}
.header2 {
    margin: -2rem 0 0 1rem;
    color:rgb(255, 255, 255);
    font-family: 'Arima Madurai';
    font-weight: 100;
    font-size: 3.7rem;
}
.card-content {
    width: 50%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
    margin: 2rem;
}
.card-snippet {
    margin-top: 2rem;
    margin-bottom: 2rem;
    font-weight: 300;
    max-width: 50vw;
}
.btn {
    max-width: 50vw;
    align-items: stretch;
}

@media (max-width: 1000px) {
    .flex-container {
        flex-direction: column;
    }
    .image-container {
        width: 100%;
        max-height: 100vh;
        border-bottom: 1px solid #6B3646;
    }
    .image {
        margin-top: -14rem; /* TODO center this */
        object-fit: cover;
        border: none;
    }
    .headers {
        position: absolute;
    }
    .card-content {
        flex-direction: column;
    }
    .card-snippet {
        margin-top: 1rem;
        max-width: 80vw;
    }
}
</style>