<script setup>

    const carousel = ref(null);
    const activeIndex = ref(0);
    const interval = ref(0);

    import { technologies } from '~/models/technologies';

    const goTo = (index) => {

        const itemWidth = carousel.value.offsetWidth;
        const scrollDistance = itemWidth * index;

        carousel.value.scrollTo({
            top: window.scrollY,
            left: scrollDistance,
            behavior: 'smooth'
        });

        activeIndex.value = index;
    }

    onMounted(() => {
        interval.value = setInterval(() => {
            console.log(activeIndex.value);
            console.log(technologies.length)
            if(activeIndex.value + 1 >= technologies.length)
                goTo(0);
            else
                goTo(activeIndex.value + 1);
        }, 2000);
    })

    onUnmounted(() => {
        clearInterval(interval.value);
    })

</script>

<template>
    <div class="grid">
        <div id="carousel" ref="carousel" class="carousel w-full">
            <div v-for="item,i in technologies" class="carousel-item w-full" :key="i">
                <div class="w-full flex justify-center">
                    <Icon size="3rem" :name="item" />
                </div>
            </div> 
        </div> 
        <div class="flex justify-center w-full py-2 gap-2">
            <button 
                v-for="item,i in technologies" class="h-3 w-3 rounded-full" :key="i"
                :class="activeIndex == i ? 'bg-slate-400':'bg-slate-200'"
                >
            </button> 
        </div>
    </div>
</template>