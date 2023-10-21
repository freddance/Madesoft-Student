<template>
  <div>

    <div class="bg-white px-10 py-6">
      <h1 class="font-bold head-text">Help Center</h1>
      <p>Get your desired help here</p>

      <div class=" mt-8">
        <div class="overview-card py-3">
          <div class="flex justify-between">
            <div>
              <div style="background: #FBFCFF; padding: 6px 12px;" class="flex gap-x-6 mx-4 mt-2">
                <div class="cursor-pointer px-2" @click="toggleType(OPTION_1)" :class="[type === OPTION_1 ? 'active' : '']">Mentor’s Help</div>
                <div class="cursor-pointer px-2" @click="toggleType(OPTION_2)" :class="[type === OPTION_2 ? 'active' : '']">Contact school</div>
              </div>
            </div>

            <div class="px-6">
              <div class="relative">
                <div class="absolute inset-y-0 left-0 flex items-center pl-3 bottom-5 md:bottom-0 pointer-events-none">
                  <svg aria-hidden="true" class="w-5 h-5 text-gray-500 dark:text-gray-400" fill="none" stroke="currentColor"
                       viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                          d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path>
                  </svg>
                </div>
                <div class="flex">
                  <div class="">
                    <input v-model="search" type="search" id="default-search"
                           class="block input p-4 pl-10  md:w-[200px]  text-sm text-gray-900 rounded-[5px]  bg-white focus:ring-none outline-none  dark:placeholder-black dark:text-black dark:focus:ring-blue-500 "
                           placeholder="Search " required>
                  </div>
                </div>


              </div>
            </div>
          </div>
        </div>
      </div>


    </div>

    <div class="">
      <div v-if="type === OPTION_1" class="mt-8">
        <HelpCenterMentorsHelp />
      </div>

      <div class="mt-8" v-if="type === OPTION_2">
        <HelpCenterContact />
      </div>
    </div>

  </div>
</template>


<script setup>
import {useQueryParamsTabSwitch} from "~/composables/useSwitchQueryParams";
import Assignment from "~/components/MyProgram/Assignment.vue";

let tabs = [
  'Mentor’s Help',
  'Contact school',

]

const type = useQueryParamsTabSwitch(tabs);
const OPTION_1 = tabs[0];
const OPTION_2 = tabs[1];

const toggleType = (_type) => {
  type.value = _type
}
</script>

<style scoped>
.overview-card {
  border-radius: 8px;
  background: var(--White, #FFF);
  box-shadow: 0px 1px 4px 0px rgba(16, 24, 40, 0.04), 0px 0.5px 3px 0px rgba(16, 24, 40, 0.04);
}

.active {
  color: #FF4155;
  border-radius: 4px;
  border: 1px solid #F8F8F8;
  background: var(--shades-white, #FFF);
  box-shadow: 0px 9px 6px -7px rgba(0, 0, 0, 0.09), 0px 0px 0px -1px rgba(0, 0, 0, 0.25);
}
</style>