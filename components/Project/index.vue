<template>
    <div id="project" class="bg-neutral-200 flex justify-center px-4 py-10 scroll-mt-12">
      <div class="md:w-10/12 lg:w-8/12">
        <h2 class="text-center font-bold pb-4">Projeto recente</h2>
        <div class="flex justify-center">
          <p class="text-justify sm:w-10/12 lg:w-8/12 2xl:w-6/12 indent-6">
            Sistema criado para que uma página do Instagram pudesse reunir seus 
            <strong>links de produto afiliado</strong> da
            Amazon em um só local, além de ferramentas, como 
            <strong>calculadora de calorias e macronutrientes.</strong> Foram desenvolvidos o front-end com <strong>nuxt</strong> 
            e o back-end com <strong>spring boot.</strong>
          </p>
        </div>
        <div class="flex justify-center">
          <img class="mockup-image w-full md:w-7/12" src="~/assets/images/mockups.png" alt="">
        </div>
        <div class="flex justify-center">
            <NuxtLink to="https://client-zefu.onrender.com/" class="btn btn-secondary text-white" type="button">Ver sistema 
                <Icon class="text-xl text-white" name="teenyicons:arrow-right-circle-solid"/>
            </NuxtLink>
        </div>
      </div>
    </div>
</template>