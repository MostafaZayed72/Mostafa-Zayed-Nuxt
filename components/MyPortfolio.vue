<template>
    <h3 class="w-[80%] mx-auto text-3xl text-center bg-slate-300 rounded-full font-bold mt-16">
        My Portfolio
    </h3>
    <p class="text-center mt-2 bg-green-500 w-40 mx-auto py-1 rounded-xl text-black">Some of my projects</p>
    <swiper :effect="'coverflow'" :grabCursor="true" :centeredSlides="true" :slidesPerView="'auto'" :coverflowEffect="{
        rotate: 50,
        stretch: 0,
        depth: 100,
        modifier: 1,
        slideShadows: true,
    }" :pagination="true" :modules="modules" class="mySwiper">
        <swiper-slide>
            <NuxtLink target="blanket" to="https://api-dev.xfit.sa/"><img class="rounded h-[250px]"
                    src="/assets/imgs/elgendy.png" />
                <h1 class="text-center text-xl font-bold mt-5">El-Gendy Project</h1>
            </NuxtLink>
        </swiper-slide>
        <swiper-slide>
            <NuxtLink target="blanket" to="https://alfa-project.vercel.app/"><img class="rounded h-[250px]"
                    src="/assets/imgs/Alfa.png" />
                <h1 class="text-center text-xl font-bold mt-5">Alfa Project</h1>
            </NuxtLink>
        </swiper-slide>
        <swiper-slide>
            <NuxtLink target="blanket" to="https://archo-chi.vercel.app/"><img class="rounded h-[250px]"
                    src="/assets/imgs/archo.png" />
                <h1 class="text-center text-xl font-bold mt-5">Archo Project</h1>
            </NuxtLink>
        </swiper-slide>
        <swiper-slide>
            <NuxtLink target="blanket" to="https://elgendy-landing.vercel.app/"><img class="rounded h-[250px]"
                    src="/assets/imgs/xfit.png" />
                <h1 class="text-center text-xl font-bold mt-5">Xfit-Saudi</h1>
            </NuxtLink>
        </swiper-slide>
        <swiper-slide>
            <NuxtLink target="blanket" to="https://leon-neon.vercel.app/"><img class="rounded h-[250px]"
                    src="/assets/imgs/Leon.png" />
                <h1 class="text-center text-xl font-bold mt-5">Leon Project</h1>
            </NuxtLink>
        </swiper-slide>
        <swiper-slide>
            <NuxtLink target="blanket" to="https://momento-inky.vercel.app/"><img class="rounded h-[250px]"
                    src="/assets/imgs/Esaal.png" />
                <h1 class="text-center text-xl font-bold mt-5">Esaal Project</h1>
            </NuxtLink>
        </swiper-slide>
        <swiper-slide>
            <NuxtLink target="blanket" to="https://ella-project-ten.vercel.app/"><img class="rounded h-[250px]"
                    src="/assets/imgs/Ellamart.png" />
                <h1 class="text-center text-xl font-bold mt-5">Ellamart+ Project</h1>
            </NuxtLink>
        </swiper-slide>
        <swiper-slide>
            <NuxtLink target="blanket" to="https://mostafazayed72.github.io/Hang-Man-Game/"><img class="rounded h-[250px]"
                    src="/assets/imgs/hang.png" />
                <h1 class="text-center text-xl font-bold mt-5">Hang-man game</h1>
            </NuxtLink>
        </swiper-slide>
        <swiper-slide>
            <NuxtLink target="blanket" to="https://mostafazayed72.github.io/Template_tow/"><img class="rounded h-[250px]"
                    src="/assets/imgs/Kasper.png" />
                <h1 class="text-center text-xl font-bold mt-5">Kasper Css project</h1>
            </NuxtLink>
        </swiper-slide>
        <swiper-slide>
            <NuxtLink target="blanket" to="https://mostafazayed72.github.io/Template_three/#Features"><img class="rounded h-[250px]"
                    src="/assets/imgs/egyptian.png" />
                <h1 class="text-center text-xl font-bold mt-5">Egyptian-Home Css project</h1>
            </NuxtLink>
        </swiper-slide>
        
    </swiper>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/effect-coverflow';
import 'swiper/css/pagination';


// import required modules
import { EffectCoverflow } from 'swiper/modules';

export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {
        return {
            modules: [EffectCoverflow],
        };
    },
};
</script>
<style>
#app {
    height: 100%
}

html,
body {
    position: relative;
    height: 100%;
}

body {
    background: #eee;
    font-family: Helvetica Neue, Helvetica, Arial, sans-serif;
    font-size: 14px;
    color: #000;
    margin: 0;
    padding: 0;
}

.swiper {
    width: 100%;
    padding-top: 50px;
    padding-bottom: 50px;
}

.swiper-slide {
    background-position: center;
    background-size: cover;
    width: 300px;
    height: 300px;
}

.swiper-slide img {
    display: block;
    width: 100%;
}
</style>