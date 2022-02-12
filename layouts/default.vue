<template>
  <div class="container">
    <TheHeader :main-name="mainName" :sub-pages="subPages" />
    <Nuxt />
  </div>
</template>

<script>
import { siteMainName, siteSubList } from '~/content/siteParams.js'

export default {
  data() {
    return {
      mainName: siteMainName,
      subPages: siteSubList,
    }
  },
}
</script>

<style>
html {
  height: 100%;
}
body {
  min-height: 100%;
  background-color: #f5f2f0;
  margin-left: 0%;
  margin-right: 0%;
}
.container {
  padding-left: 0;
  padding-right: 0;
  font-family: Roboto, sans-serif;
  font-weight: 100;
  min-width: 100%;
  max-width: 100vw;
  position: relative;
  align-items: center;
  justify-content: space-between;
}
</style>
