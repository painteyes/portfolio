<template>
    <div class="py-5 text-center">
        <div class="container max-w-screen-lg mx-auto">
            <div>
                <div class="flex flex-wrap justify-center gap-2">

                    <a href="#">
                        <img 
                        src="/src/assets/icon-youtube.svg" 
                            class="logo bg-stone-400 p-2 font-semibold text-white inline-flex items-center space-x-2" 
                            alt="Youtube" 
                        />
                    </a>

                    <a href="#">
                        <img 
                            src="/src/assets/icon-linkedin.svg" 
                            class="logo bg-stone-400 p-2 font-semibold text-white inline-flex items-center space-x-2" 
                            alt="Linkedin" 
                        />
                    </a>

                    <a href="#">
                        <img 
                            src="/src/assets/icon-twitter.svg"
                            class="logo bg-stone-400 p-2 font-semibold text-white inline-flex items-center space-x-2" 
                            alt="Twitter" 
                        />
                    </a>

                    <a href="#">
                        <img 
                            src="/src/assets/icon-github.svg" 
                            class="logo bg-stone-400 p-2 font-semibold text-white inline-flex items-center space-x-2" 
                            alt="Github" 
                        />
                    </a>
                
                </div>
            </div>
        </div>
    <p class="text-sm mt-2  opacity-50">
        &copy; {{new Date().getFullYear()}} Andrea Occhipinti. All rights reserved.
    </p>
</div>
</template>

<style scoped>
.logo {
    border-radius: 10px;
    will-change: filter;
    transition: filter 300ms;
}
.logo:hover {
    filter: drop-shadow(0 0 0.2em rgb(195, 195, 195));
}
</style>