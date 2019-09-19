<template>
    <div id="app">
        <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
        <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
        <h1>
            <a @click="mailto()" :title="name">{{ name }}</a>
        </h1>
    </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'



export default {
    name: 'app',
    //   components: {
    //     HelloWorld
    //   },
    data() {
        return {
            name: 'NOVUS IDEA',
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
body {
    font-family: 'Megrim', sans-serif;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    margin: 0;
}

h1 {
    margin: 0;
}

h1 a {
    color: #777;
    font-size: 2rem;
    font-weight: 100;
    text-decoration: none;
    display: inline-block;
    cursor: pointer;
    padding: 2rem;
}
// #app {
//   font-family: 'Avenir', Helvetica, Arial, sans-serif;
//   -webkit-font-smoothing: antialiased;
//   -moz-osx-font-smoothing: grayscale;
//   text-align: center;
//   color: #2c3e50;
//   margin-top: 60px;
// }
</style>
