<script setup>
import { ref, onMounted } from 'vue';
import MoonIcon from '/src/assets/icon-moon.svg';
import SunIcon from '/src/assets/icon-sun.svg';

const isDarkMode = ref(false);

const initializeTheme = () => {
    const userTheme = localStorage.getItem("theme");
    const prefersDark = window.matchMedia("(prefers-color-scheme: dark)").matches;
    isDarkMode.value = userTheme === "dark" || (!userTheme && prefersDark);
    applyTheme();
};

const applyTheme = () => {
    if (isDarkMode.value) {
        document.documentElement.classList.add('dark');
        localStorage.setItem("theme", 'dark');
    } else {
        document.documentElement.classList.remove('dark');
        localStorage.setItem("theme", 'light');
    }
};

const toggleTheme = () => {
    isDarkMode.value = !isDarkMode.value;
    applyTheme();
};

onMounted(initializeTheme);

</script>

<template>
    <button 
        @click="toggleTheme" 
        aria-label="Toggle theme" 
        class="fixed p-2 z-10 right-20 top-4 bg-violet-300 dark:bg-orange-300 text-lg rounded-md"
    >
        <SunIcon v-if="isDarkMode" />
        <MoonIcon v-else />
    </button>
</template>