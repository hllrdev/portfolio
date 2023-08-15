<script setup>
  const carousel = ref(null);
  const activeIndex = ref(0);
  const interval = ref(0);

  const technologies = [
    "skill-icons:html",
    "skill-icons:javascript",
    "skill-icons:tailwindcss-light",
    "skill-icons:vuejs-light",
    "skill-icons:nuxtjs-light",
    "skill-icons:spring-light",
    "skill-icons:java-light",
    "skill-icons:python-light",
    "skill-icons:figma-light",
  ];

  const goTo = (index) => {
    const itemWidth = carousel.value.offsetWidth;
    const scrollDistance = itemWidth * index;

    carousel.value.scrollTo({
      top: window.scrollY,
      left: scrollDistance,
      behavior: "smooth",
    });

    activeIndex.value = index;
  };

  onMounted(() => {
    interval.value = setInterval(() => {
      if (activeIndex.value + 1 >= technologies.length / 3) goTo(0);
      else goTo(activeIndex.value + 1);
    }, 3000);
  });

  onUnmounted(() => {
    clearInterval(interval.value);
  });
</script>

<template>
  <div class="grid">
    <div id="carousel" ref="carousel" class="carousel w-full pb-2">
      <div
        v-for="(item, i) in technologies.length / 3"
        class="carousel-item w-full"
        :key="i">
        <div class="w-full flex justify-center gap-4 text-5xl">
          <Icon :name="technologies[i * 3]" />
          <Icon :name="technologies[i * 3 + 1]" />
          <Icon :name="technologies[i * 3 + 2]" />
        </div>
      </div>
    </div>
    <div class="flex justify-center w-full py-2 gap-2">
      <button
        v-for="(item, i) in technologies.length / 3"
        class="h-3 w-3 rounded-full"
        :key="i"
        :class="activeIndex == i ? 'bg-slate-400' : 'bg-slate-200'"
      ></button>
    </div>
  </div>
</template>
