<template>
        <b-navbar toggleable="md" type="light" sticky class="top-nav">
            <b-navbar-brand href="#">Beauty Salon</b-navbar-brand>
            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
            <b-collapse id="nav-collapse" is-nav>
            <!-- Right aligned nav items -->
            <b-navbar-nav class="ml-auto">
                <b-nav-item href="#">About Us</b-nav-item>
                <b-nav-item href="#">Services</b-nav-item>
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
    background-color: rgba(255, 255, 255, 0.747);
    border-bottom: 1px solid rgb(236, 233, 233);
}

</style>