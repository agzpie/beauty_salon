<template>
    <div class="card-container">
        <kinesis-container event="scroll">
            <kinesis-element :strength="10">
              <img :src="require(`@/assets/images/${ card.image || 'image_1.jpg'}`)" alt="some image" class="image">
            </kinesis-element>

            <kinesis-element :strength="100" :type="translate" axis="y">
              <h1 class="header1"> {{ card.title }} </h1>
            </kinesis-element>

            <kinesis-element :strength="180" :type="depth_inv" axis="y">  
              <h1 class="header2"> {{ card.title }} </h1>
            </kinesis-element>
            
            <p class="snippet"> {{ card.snippet }} </p>

            <div class="btn">
                <OutlineButton> {{ card.button }} </OutlineButton>
            </div>
        </kinesis-container>
    </div> 
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
    .card-container {
        display: flex;
        padding: 0 0;
        align-items: center;
        justify-content: space-between;
        margin: 4rem 0 1rem 0;
        
    }
    .image {
        max-width: 100vw;
        margin: 0 -3rem;
    }
    .header1 {
        margin: -3rem 0 -2rem 0;
        color:white;
    }
    .header2 {
        margin: -2rem 0 0 0;
        color:rgb(146, 100, 129);
    }
    .snippet {
        margin: 4rem 0;
    }
    .btn {
        width: 100%;
        align-items: stretch;
    }

</style>