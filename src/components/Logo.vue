<template>
    <div id="Logo">
        <a v-if="link" :href="link" :title="title">
            <img :src="image" :alt="title" :width="width" :height="height">
        </a>
        <img v-else :src="image" :alt="title" :width="width" :height="height">
    </div>
</template>

<script>
export default {
    name: 'Logo',
    props: {
        title: {
            type: String,
            default: null,
        },
        image: {
            type: String,
            default: null,
        },
        link: {
            type: String,
            default: null,
        },
        width: {
            type: String,
            default: '100',
        },
        height: {
            type: String,
            default: '100',
        },
    },
}
</script>

<style lang="scss">
#Logo {
    animation-name: pulse;
    animation-duration: 3000ms;
    animation-iteration-count: infinite;
    transform: scale(0.9);
    opacity: 0.5;
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
