<template>

    <!-- <div id="nav">
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
    </div> -->

    <img id="Logo" :src="$store.state.logo" :title="$store.state.name" :alt="$store.state.name">

    <a class="contact" @click="mailto()" :title="$store.state.name">@</a>

    <!-- <router-view/> -->

</template>

<script>
export default {
    name: 'app',
    methods: {
        mailto() {
            window.location = 'mailto:' + this.$store.state.email;
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

#Logo {
    animation-name: pulse;
    animation-duration: 3000ms;
    animation-iteration-count: infinite;
    transform: scale(0.9);
    width: 100px;
    height: 100px;
    opacity: 0.5;
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

@keyframes pulse {
    0% {
        transform: scale(0.9);
        opacity: 0.5;
    }
    50% {
        transform: scale(1);
        opacity: 1;
    }
    100% {
        transform: scale(0.9);
        opacity: 0.5;
    }
}
</style>
