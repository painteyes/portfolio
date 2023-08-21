<script setup>
import timeline from '../data/timeline';
import TimelineItem from './TimelineItem.vue';


</script>

<template>
    <div class="flex flex-col md:flex-row justify-center my-20">
        <div class="w-full md:w-7/12">
            <h1 class="text-2xl font-bold underline underline-offset-8 decoration-4 mb-5 text-stone-900 dark:text-white">
                Timeline
            </h1>
            <TimelineItem v-for="item in timeline"
                :year="item.year"               
                :title="item.title"
                :duration="item.duration"
                :details="item.details"
            />
         </div>
      </div>
</template>