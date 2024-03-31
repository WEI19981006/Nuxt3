<template>
    <div class="">
        <header class="w-full bg-slate-400 py-2 flex items-center justify-between px-5">
            <h1 class=" text-3xl">Logo</h1>
            <nav class=" flex gap-2">
                <NuxtLink to="/" class="block px-3 py-2  box-border" :class="{ ' border-b-2': isActive('/') }">首頁
                </NuxtLink>
                <NuxtLink to="/about" class=" block px-3 py-2" :class="{ 'border-b-2': isActive('/about') }">About
                </NuxtLink>
            </nav>
        </header>
        <slot></slot>
    </div>
</template>

<script setup>
import { useRoute } from "vue-router";
const route = useRoute();
function isActive(path) {
    return route.path === path;
};
</script>