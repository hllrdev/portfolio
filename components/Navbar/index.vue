<template>
  <nav>
    <div class="navbar bg-base-100 p-8 hidden md:flex">
      <div class="flex-1">
        <UiLogo />
      </div>
      <NavbarMenu />
    </div>
    <div class="drawer md:hidden">
      <input id="my-drawer" type="checkbox" class="drawer-toggle" />
      <div class="w-screen sticky">
        <div class="p-4 flex items-center justify-center">
          <label class="absolute left-6" for="my-drawer">
            <Icon name="iconoir:menu" size="1.75rem" />
          </label>
          <UiLogo />
        </div>
      </div>
      <div class="drawer-side z-50">
        <label for="my-drawer" class="drawer-overlay"></label>
        <div class="menu p-4 w-80 h-full bg-neutral text-base-content">
          <NavbarMenu class="text-base-100" />
        </div>
      </div>
    </div>
  </nav>
</template>
