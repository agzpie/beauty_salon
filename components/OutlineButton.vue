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
    font-variant: small-caps;
    display: inline-block;
    margin: 0.5rem;
    padding: 0.75em 1.5em;
    border: 1px solid rebeccapurple;
    border-radius: 3px;
    background-color: transparent;
    color:rgb(88, 68, 105);
    font-size: 1.25em;
    font-weight: 400;
    transition: 0.4s;
    letter-spacing: 0.02em;
  }

  .button:hover {
    background: rebeccapurple;
    color: whitesmoke;
    padding: 1em 2em;
    letter-spacing: 0.04em;
  }
</style>