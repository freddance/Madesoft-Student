<template>
  <div class=" mt-8">
    <div class="bg-white mx-10  py-2">
      <h1 class="font-medium text-lg pt-4 px-6">Manage Subscription & Billing History</h1>

      <div class="px-6 gap-16">
        <div class=" certificate mt-12 pb-6">
           <div class="px-8 py-4 text-white">
             <h1 style="opacity: 0.6;">Your Subscription</h1>
             <h1 class="pt-2 font-medium">
               MAT CIAPP - Certificate in Industrial Automation and PLC Programming
             </h1>

             <div class="flex text-xs pt-8">
               Enrolled on: 14th July 2023 ------ Expiring on: 14th July 2023
             </div>
           </div>

          <div class="bg-white py-1 text-sm mt-6 text-center">
            Cancel subscription
          </div>

          <div class="px-8  text-white">
            <h1 class="pt-4 font-semibold">
              Price: N345,000
            </h1>

          </div>
        </div>

      </div>


      <h1 class="font-medium text-lg pt-16 px-6">Billing History</h1>
      <div class="card mt-4">
        <DataTable :value="customers" paginator :rows="5" dataKey="id" :rowsPerPageOptions="[5, 10, 20, 50]" tableStyle="min-width: 50rem">

          <Column   headerStyle="width: 3rem">
            <template #body="{ data }">
              <div>
                <Checkbox  @click="OptionsModal = true" :binary="true" class="mt-0" />
              </div>
            </template>
          </Column>
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
<!--                <img src="~assets/images/times-Icons.svg" class="flex justify-end ml-auto cursor-pointer relative bottom-1"-->
<!--                     @click="OptionsModal = false" alt="">-->
              </div>
            </div>

          </div>
        </Dialog>
      </div>
    </div>
  </div>
</template>


<script setup>
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
.input {
  border-radius: 8px;
  border: 1px solid var(--neutral-100, #E7EAEE);
  background: #FBFBFB;
}

.certificate{
  border-radius: 8px;
  background: #55000A;
  width: 451px;
}
</style>