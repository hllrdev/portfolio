<template>
  <header class="flex md:justify-center px-4 md:p-0 flex-grow">
    <div class="md:w-11/12 lg:w-9/12 grid">
      <div
        class="pt-16 md:pt-0 flex flex-col md:flex-row items-center md:items-end justify-around"
      >
        <div>
          <h1>Héuller</h1>
          <h2 class="text-primary">desenvolvedor web full stack</h2>
        </div>
        <div class="w-60 md:w-72">
          <img src="~/assets/images/me_b&w.png" alt="Foto do autor do portfólio" />
        </div>
      </div>
      <div class="flex items-end">
        <div class="flex justify-between w-full">
          <div class="flex items-center gap-4 text-2xl">
            <Icon name="teenyicons:linkedin-solid" color="#0E76A8" />
            <Icon name="teenyicons:github-solid" />
            <Icon name="teenyicons:instagram-solid" color="#fb3958" />
          </div>
          <div>
            <h4>hllrdev@gmail.com</h4>
          </div>
        </div>
      </div>
      <div class="grid items-end">
        <HeaderCarousel />
      </div>
    </div>
  </header>
</template>
