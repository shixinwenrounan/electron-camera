<!--  -->
<template>
    <main>
        <video></video>
    </main>
</template>

<script setup lang="ts">
// const devices = await navigator.mediaDevices.enumerateDevices();
// console.log(devices);

import { onMounted } from "vue";

// Put variables in global scope to make them available to the browser console.
onMounted(() => {
    const constraints = {
        audio: false,
        video: true,
    };

    const video = document.querySelector("video")!;

    navigator.mediaDevices.getUserMedia(constraints).then((stream) => {
        video.srcObject = stream;
        video.play();
    });
});

</script>
<style lang="scss" scoped>
</style>