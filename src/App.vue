<script setup>
import Intro from './components/Intro.vue'
import Portfolio from './components/Portfolio.vue'
import Timeline from './components/Timeline.vue';
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="bg-white dark:bg-stone-900 text-stone-900 dark:text-stone-300 min-h-screen font-inter">
	  <div class="max-w-5xl w-11/12 mx-auto">
      <Intro />
      <Portfolio />
      <Timeline />
      <Contact />
      <Footer /> 
		</div>
	</div>
</template>


