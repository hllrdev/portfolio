<template>
  <header id="start" class="pt-20 md:pt-0 px-4 h-full md:flex md:justify-center md:items-end">
    <div class="md:w-10/12 lg:w-8/12 md:h-5/6 md:grid h-full grid">
      <div class="md:grid md:grid-flow-col md:items-center md:justify-between grid items-end justify-center">
        <div>
          <h1>Héuller</h1>
          <h2 class="text-primary">desenvolvedor web full stack</h2>
          <h3 class="text-base py-2 md:pr-4 font-normal">Tenho 25 anos e programo desde os meus 17. Busco entregar <strong>soluções simples e eficientes.</strong></h3>
        </div>
        <div class="w-60 md:w-72">
          <img src="~/assets/images/me_b&w.png" alt="Foto do autor do portfólio" />
        </div>
      </div>
      <div class="flex items-center">
        <div class="w-full flex justify-between py-2">
          <UiSocialMedia/>
          <div class="flex items-center">
            <h4>hllrdev@gmail.com</h4>
          </div>
          
        </div>
      </div>
      <div class="flex justify-center items-end">
        <HeaderCarousel />
      </div>
    </div>
  </header>
</template>
