<template>

    <!-- <div id="nav">
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
    </div> -->

    <logo :image="logo" title="NOVUS IDEA" />

    <a class="contact" @click="mailto()" :title="name">@</a>

    <!-- <router-view/> -->

</template>

<script>
import Logo from './components/Logo.vue'

export default {
    name: 'app',
    components: {
        logo: Logo
    },
    data() {
        return {
            name: 'NOVUS IDEA',
            logo: require('./assets/logo.svg'),
            email: 'mail@novusidea.de',
        }
    },
    methods: {
        mailto() {
            window.location = 'mailto:' + this.email;
        },
    }
}
</script>

<style lang="scss">
html {
    font-size: 20px;
}

body {
    font-family: 'Megrim', cursive;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    line-height: 1.4;
    font-size: 1rem;
    height: 100vh;
    margin: 0;
}

a {
    color: #777;
    text-decoration: none;
    display: inline-block;
    cursor: pointer;
}

.contact {
    font-family: 'Arial' , sans-serif;
    font-weight: 400;
    font-size: 0.9rem;
    color: #ccc;
    position: absolute;
    bottom: 30px;
    right: 30px;

    &:hover {
        color: #aaa;
    }
}
</style>
