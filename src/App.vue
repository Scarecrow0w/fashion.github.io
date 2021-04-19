<template>
<Navbar />
<Header />
<section class="flex flex-wrap">
    <Articles />
    <SideInfo />
</section>  
<Footer />
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import Header from './components/Header.vue'
import Articles from './components/Articles.vue'
import SideInfo from './components/SideInfo.vue'
import Footer from './components/Footer.vue'

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
</script>

<style scoped>
    section {
        padding-top: 60px;
    }
</style>
