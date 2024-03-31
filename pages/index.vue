<template>
    <div class="container mx-auto">
        <h1>首頁</h1>
        <p>高度:{{ size.height }}</p>
        <p>寬度:{{size.width}}</p>


    </div>
</template>

<script setup>
    import {useWindowSize} from "@vueuse/core"
    const size = useWindowSize();
    onMounted(() => {
        console.log(size);
    });
</script>

<style scoped>

</style>