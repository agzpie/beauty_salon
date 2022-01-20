<template>
        <b-navbar toggleable="md" type="light" class="top-nav">
            <b-navbar-brand href="#">
                <NuxtLink to="/">Beauty Salon</NuxtLink>
            </b-navbar-brand>
            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
            <b-collapse id="nav-collapse" is-nav>
            <!-- Right aligned nav items -->
            <b-navbar-nav class="ml-auto">
                <b-nav-item href="#">
                    <NuxtLink to="/about">About Us</NuxtLink>
                </b-nav-item>
                <b-nav-item href="#">
                    <NuxtLink to="/services">Services</NuxtLink>    
                </b-nav-item>
                <b-nav-item href="#">Gallery</b-nav-item>
                <b-nav-item href="#">Contact</b-nav-item>
            </b-navbar-nav>
            </b-collapse>
        </b-navbar>
</template>

<script>


export default {

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