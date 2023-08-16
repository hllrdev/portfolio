<template>
    <div class="flex gap-4 text-2xl">
        <NuxtLink to="#">
            <Icon name="teenyicons:linkedin-solid"/>
        </NuxtLink>
        <NuxtLink to="#">
            <Icon name="teenyicons:github-solid" />
        </NuxtLink>
        <NuxtLink to="#">
            <Icon name="teenyicons:instagram-solid"/>
        </NuxtLink>
    </div>
</template>

<style scoped>
    a {
        @apply hover:-translate-y-2 duration-200
    }
</style>