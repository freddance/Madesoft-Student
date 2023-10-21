<template>
  <div>
    <div class="flex px-2">
      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
        <path d="M10.875 19.3L4.27502 12.7C4.17502 12.6 4.10402 12.4917 4.06202 12.375C4.02002 12.2583 3.99935 12.1333 4.00002 12C4.00002 11.8667 4.02102 11.7417 4.06302 11.625C4.10502 11.5083 4.17568 11.4 4.27502 11.3L10.875 4.7C11.0583 4.51667 11.2877 4.421 11.563 4.413C11.8383 4.405 12.0757 4.50067 12.275 4.7C12.475 4.88333 12.5793 5.11267 12.588 5.388C12.5967 5.66333 12.5007 5.90067 12.3 6.1L7.40002 11H18.575C18.8583 11 19.096 11.096 19.288 11.288C19.48 11.48 19.5757 11.7173 19.575 12C19.575 12.2833 19.4793 12.521 19.288 12.713C19.0967 12.905 18.859 13.0007 18.575 13H7.40002L12.3 17.9C12.4833 18.0833 12.5793 18.3167 12.588 18.6C12.5967 18.8833 12.5007 19.1167 12.3 19.3C12.1167 19.5 11.8833 19.6 11.6 19.6C11.3167 19.6 11.075 19.5 10.875 19.3Z" fill="#FF4155"/>
      </svg>
      <span style="color: #FF4155;">Back</span>
    </div>

    <h1 class="font-bold text-lg mt-8">Assignments</h1>
  </div>
  <div class="card mt-4">
    <DataTable :value="customers" paginator :rows="5" dataKey="id" :rowsPerPageOptions="[5, 10, 20, 50]" tableStyle="min-width: 50rem">

      <Column field="id" header="S/N" headerStyle="width: 3rem"></Column>
      <Column field="name" header="Name" style="width: 25%"></Column>
      <Column field="country.name" header="Country" style="width: 25%"></Column>
      <Column field="company" header="Company" style="width: 25%"></Column>
      <Column field="representative.name" header="Representative" style="width: 25%"></Column>
      <Column field="status" header="Status" :showFilterMenu="false" :filterMenuStyle="{ width: '14rem' }" style="min-width: 12rem">
        <template #body="{ data }">
          <div :value="data.status" :class="[status === completed ? 'completed' : 'incomplete']">{{data.status}}</div>
        </template>
      </Column>

      <Column   headerStyle="width: 5rem" style="width: 25%">
        <template #body="{ data }">
          <div>
            <Menu as="div" class="relative">
              <div>
                <MenuButton class="flex gap-4">
                  <button class="w-full ">
                    <svg xmlns="http://www.w3.org/2000/svg" width="4" height="18" viewBox="0 0 4 18" fill="none">
                      <rect width="4" height="3.6" fill="#101010"/>
                      <rect y="7.2002" width="4" height="3.6" fill="#101010"/>
                      <rect y="14.3999" width="4" height="3.6" fill="#101010"/>
                    </svg>
                  </button>

                </MenuButton>
              </div>
              <transition enter-active-class="transition ease-out duration-100" enter-from-class="transform opacity-0 scale-95" enter-to-class="transform opacity-100 scale-100" leave-active-class="transition ease-in duration-75" leave-from-class="transform opacity-100 scale-100" leave-to-class="transform opacity-0 scale-95">
                <MenuItems class="absolute right-0 z-10 mt-2 w-48 origin-top-right rounded-md bg-white py-1 shadow-lg  ring-opacity-5 focus:outline-none">
                  <MenuItem v-slot="{ active }">
                    <nuxt-link to="/my-program/view-submission" :class="[active ? 'bg-gray-100' : '', 'block px-4 py-2 text-sm text-gray-700 cursor-pointer']">View Submission</nuxt-link>
                  </MenuItem>
                  <MenuItem>
                    <h6 :class="[active ? 'bg-gray-100' : '', 'block px-4 py-2 text-sm text-gray-700 cursor-pointer']">Download</h6>
                  </MenuItem>
                </MenuItems>
              </transition>
            </Menu>
          </div>
        </template>
      </Column>
    </DataTable>
  </div>

  <div class="options">
    <Dialog v-model:visible="OptionsModal" modal header="" :dismissableMask="true" :closable="false" class="md:w-auto w-96 ">
      <div class="py-6 px-4" style="background: #323A46; width: auto!Important; border-radius: 5px;">
        <div>
          <div class="lg:flex gap-4 align-middle place-content-center">
            <div>
              <span class=" text-center cursor-pointer px-4 pt-2 pb-2 text-xs"
                    style="border: 1px solid #525252; border-radius: 5px; color: #E1E8F9;">
                Delete
              </span>
            </div>
            <div>
              <span class=" text-center cursor-pointer px-4 pt-2 pb-2 text-xs"
                    style="border: 1px solid #525252; border-radius: 5px; color: #E1E8F9;">
                Edit
              </span>
            </div>
            <img src="~assets/images/times-Icons.svg" class="flex justify-end ml-auto cursor-pointer relative bottom-1"
                 @click="OptionsModal = false" alt="">
          </div>
        </div>

      </div>
    </Dialog>
  </div>
</template>

<script setup>
import {  Menu, MenuButton, MenuItem, MenuItems } from '@headlessui/vue'
import { ref, onMounted } from 'vue';

const OptionsModal = ref(false)


const customers = ref([
  {
    id: 1,
    name: 'James Butt',
    country: {
      name: 'Algeria',
      code: 'dz'
    },
    company: 'Benton, John B Jr',
    date: '2015-09-13',
    status: 'completed',
    verified: true,
    activity: 17,
    representative: {
      name: 'Ioni Bowcher',
      image: 'ionibowcher.png'
    },
    balance: 70663
  },

]);

</script>


<style>


.completed {
  border-radius: 20px;
  background: var(--success-50, #ECFDF3);
  color: var(--success-500, #12B76A);
  padding: 8px 19px;
  width: 107px;
}

.Incomplete {
  border-radius: 20px;
  background: var(--warning-50, #FFFAEB);
  color: var(--warning-500, #F79009);
  padding: 8px 19px;
  width: 107px;

}
</style>