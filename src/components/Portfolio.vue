<script setup>
import portfolio from '../data/portfolio';
import PortfolioItem from './PortfolioItem.vue';

</script>

<template>
    <div class="flex flex-col md:flex-row items-center justify-center">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
            <PortfolioItem v-for="project in portfolio"
                :key="project.id"
                :imgUrl="project.imgUrl"
                :title="project.title"
                :stack="project.stack"
                :link="project.link"
            />
        </div>
    </div>
</template>

