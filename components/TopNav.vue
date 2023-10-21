<template>
  <div class="w-full bg-white " >
    <div class="md:px-8 py-2 flex">
      <h1 style="color: #360040" class="font-bold text-xl pt-3 move lg:ml-0 ml-20">
        <slot>

        </slot>
      </h1>

      <div class="flex justify-end ml-auto mt-1">
        <nuxt-link  to="/cart" type="button"
                   class="relative inline-flex items-center p-3 text-sm mr-6 font-medium text-center text-white ">
          <img src="~assets/images/bell.svg" class="w-5" alt="">
          <span class="sr-only">Notifications</span>
          <div
              class="absolute inline-flex items-center justify-center w-5 h-5 text-xs font-bold text-white border-2 border-white rounded-full -top-0 -right-1 " style="background: #ED405C;">
           1
          </div>
        </nuxt-link>

        <!-- Profile dropdown -->
        <Menu as="div" class="relative ml-3 lg:mr-0 mr-8">
          <div>
            <MenuButton class="flex">
              <img src="~assets/images/Avatar.svg" alt="">
              <img src="~assets/images/arrow-down.svg" class="mt-2" alt="">
            </MenuButton>
          </div>
          <transition enter-active-class="transition ease-out duration-100" enter-from-class="transform opacity-0 scale-95" enter-to-class="transform opacity-100 scale-100" leave-active-class="transition ease-in duration-75" leave-from-class="transform opacity-100 scale-100" leave-to-class="transform opacity-0 scale-95">
            <MenuItems class="absolute right-0 z-10 mt-2 w-48 origin-top-right rounded-md bg-white py-1 shadow-lg  ring-opacity-5 focus:outline-none">
              <MenuItem v-slot="{ active }">
                <nuxt-link to="/profile" :class="[active ? 'bg-gray-100' : '', 'block px-4 py-2 text-sm text-gray-700']">Your Profile</nuxt-link>
              </MenuItem>
              <MenuItem>
                <h6 class="'block px-4 py-2 text-sm text-gray-700'">Olu Alfred</h6>
              </MenuItem>
              <MenuItem v-slot="{ active }">

                <a  :class="[active ? 'bg-gray-100' : '', 'block px-4 py-2 text-sm text-gray-700']">Sign out</a>
              </MenuItem>
            </MenuItems>
          </transition>
        </Menu>
      </div>
    </div>
  </div>
</template>

<script setup>
import {  Menu, MenuButton, MenuItem, MenuItems } from '@headlessui/vue'

</script>

<style scoped>
nav {
  /*height: 76px;*/
  /*background: #FFFFFF;*/
  /*box-shadow: 0px 3px 7px rgba(0, 0, 0, 0.06);*/
  /*padding: 0 24px;*/
  display: flex;
  align-items: center;
  grid-gap: 24px;
  font-family: var(--lato);
  position: sticky;
  top: 0;
  left: 0;
  z-index: 1000;
}

nav::before {
  content: '';
  position: absolute;
  width: 40px;
  height: 40px;
  bottom: -40px;
  left: 0;
  /*border-radius: 50%;*/
  box-shadow: -20px -20px 0 var(--light);
}
</style>