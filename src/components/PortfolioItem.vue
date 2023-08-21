<script setup>

const props = defineProps({
    title: String,
    imgUrl: String,
    stack: Array,
    link: String
})

</script>

<template>
    <a 
        :href="link"
        target="_blank"
        rel="noopener noreferrer"
        class="border-2 border-stone-900 dark:border-white rounded-md overflow-hidden"
      >
         <img
            :src="imgUrl"
            alt="preview" 
            class="w-full h-36 md:h-48 object-cover cursor-pointer"
         />
         <div class="w-full p-4">
            <h3 class="text-lg md:text-xl dark:text-white mb-2 md:mb-3 font-semibold ">{{title}}</h3>
            <p class="flex flex-wrap gap-2 flex-row items-center justify-start text-xs md:text-sm dark:text-white ">
                <span v-for="item in stack" class="inline-block px-2 py-1 font-semibold border-2 border-stone-900 dark:border-white rounded-md">
                    {{item}}
                </span>
            </p>
         </div>
    </a>
</template>