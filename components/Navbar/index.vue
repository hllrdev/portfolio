<template>
  <div>
    <div class="navbar bg-base-100 px-6 hidden md:flex fixed border-b z-50">
      <div class="flex-1">
        <UiLogo />
      </div>
      <NavbarMenu />
    </div>
    <div class="drawer bg-base-100 md:hidden border-b fixed left-0 z-50">
      <input id="my-drawer" type="checkbox" class="drawer-toggle" />
      <div class="w-screen sticky">
        <div class="p-4 flex items-center justify-center">
          <label class="absolute left-6 text-2xl" for="my-drawer">
            <Icon name="iconoir:menu" />
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
  </div>
</template>
