<template>
    <div class="flex gap-4 text-2xl">
        <NuxtLink to="https://www.linkedin.com/in/heuller-soares/">
            <Icon name="teenyicons:linkedin-solid"/>
        </NuxtLink>
        <NuxtLink to="https://github.com/hllrdev">
            <Icon name="teenyicons:github-solid" />
        </NuxtLink>
        <NuxtLink to="https://www.instagram.com/heullersuarez/">
            <Icon name="teenyicons:instagram-solid"/>
        </NuxtLink>
    </div>
</template>

<style scoped>
    a {
        @apply hover:-translate-y-2 duration-200
    }
</style>