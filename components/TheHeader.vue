<template>
  <header>
    <b-navbar toggleable="md" type="light" class="top-nav">
      <b-navbar-brand>
        <NuxtLink to="/">{{ mainName }}</NuxtLink>
      </b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-item v-for="page in subPages" :key="page.name">
            <NuxtLink :to="`${page.url}`">{{ page.name }}</NuxtLink>
          </b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </header>
</template>

<script>
export default {
  props: {
    mainName: {
      type: String,
      required: true,
      default: () => '',
    },
    subPages: {
      type: Array,
      required: true,
      default: () => [],
    },
  },
}
</script>

<style>
.top-nav {
  position: fixed;
  width: 100vw;
  font-family: 'Arima Madurai';
  font-weight: 300;
  background-color: rgba(255, 255, 255, 0.205);
  border-bottom: 1px solid rgb(236, 233, 233);
  z-index: 10;
}
</style>
