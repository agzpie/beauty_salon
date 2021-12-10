<template>
  <button class="button">
    <slot/>
  </button>
</template>

<script>
export default {

}
</script>

<style>
  .button {
    font-family: 'Arima Madurai';
    font-variant: small-caps;
    display: inline-block;
    margin: 0.5rem;
    padding: 0.75em 1.5em;
    border: 1px solid #6B3646;
    border-radius: 3px;
    background-color: transparent;
    color:#6B3646;
    font-size: 1.25em;
    font-weight: 600;
    transition: 0.4s;
    letter-spacing: 0.02em;
  }

  .button:hover {
    background: #6B3646;
    color: whitesmoke;
    padding: 1em 2em;
    letter-spacing: 0.05em;
  }
</style>