<template>
  <div>

    <div class="px-10 mt-8">
      <div class="flex">
        <div class="flex px-2">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
            <path d="M10.875 19.3L4.27502 12.7C4.17502 12.6 4.10402 12.4917 4.06202 12.375C4.02002 12.2583 3.99935 12.1333 4.00002 12C4.00002 11.8667 4.02102 11.7417 4.06302 11.625C4.10502 11.5083 4.17568 11.4 4.27502 11.3L10.875 4.7C11.0583 4.51667 11.2877 4.421 11.563 4.413C11.8383 4.405 12.0757 4.50067 12.275 4.7C12.475 4.88333 12.5793 5.11267 12.588 5.388C12.5967 5.66333 12.5007 5.90067 12.3 6.1L7.40002 11H18.575C18.8583 11 19.096 11.096 19.288 11.288C19.48 11.48 19.5757 11.7173 19.575 12C19.575 12.2833 19.4793 12.521 19.288 12.713C19.0967 12.905 18.859 13.0007 18.575 13H7.40002L12.3 17.9C12.4833 18.0833 12.5793 18.3167 12.588 18.6C12.5967 18.8833 12.5007 19.1167 12.3 19.3C12.1167 19.5 11.8833 19.6 11.6 19.6C11.3167 19.6 11.075 19.5 10.875 19.3Z" fill="#FF4155"/>
          </svg>
          <span style="color: #FF4155;">Back</span>
        </div>

      </div>


      <div class="bg-white px-4 py-4 mt-8 ">
        <div class="quiz">
          <div class="font text-white flex justify-between text-xl mt-2" style="background: #FF4155; padding: 25px 16px 25px 22px;">
            <div class="flex gap-4">
              <div class="font-bold">Quiz:</div>
              Equipment’s Used In Industrial Automation
            </div>

            <div class="flex gap-4">
              <div class="font-bold">Total questions:</div> 12
            </div>
          </div>

          <div class=" ">
            <div class="border-b py-8 ">
              <h2 class="mx-12 flex gap-2"> <div class="font-bold">Question 1:</div> What is Industrial Automation</h2>
            </div>

            <div class=" pt-8 pb-10">
              <div class="flex mt-6 px-12 border-b pb-10">
                <Checkbox v-model="checked" :binary="true" class="mt-2" />
                <div class="px-4">
                  This is a high-level pictorial view of a PLC dishing 1's and 0's to an industrial plant
                  conveyor with a counter counting the packets as they pass through a sensor.
                </div>
              </div>

              <div class="flex mt-12 px-12 border-b pb-10">
                <Checkbox v-model="checked" :binary="true" class="mt-2" />
                <div class="px-4">
                  This is a high-level pictorial view of a PLC dishing 1's and 0's to an industrial plant
                  conveyor with a counter counting the packets as they pass through a sensor.
                </div>
              </div>

              <div class="flex mt-12 px-12 border-b pb-10">
                <Checkbox v-model="checked" :binary="true" class="mt-2" />
                <div class="px-4">
                  This is a high-level pictorial view of a PLC dishing 1's and 0's to an industrial plant
                  conveyor with a counter counting the packets as they pass through a sensor.
                </div>
              </div>

              <div class="flex mt-12 px-12 border-b pb-10">
                <Checkbox v-model="checked" :binary="true" class="mt-2" />
                <div class="px-4">
                  This is a high-level pictorial view of a PLC dishing 1's and 0's to an industrial plant
                  conveyor with a counter counting the packets as they pass through a sensor.
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="flex justify-between mt-8">
          <div>
            <button class="nobg-btn w-[170px]">Previous</button>
          </div>
          <div>
            <MadesoftButton title="Next" is-loading="" class="w-[170px]"></MadesoftButton>
          </div>
        </div>
      </div>


    </div>

  </div>
</template>


<script setup>

import MadesoftButton from "~/components/MadesoftButton.vue";

const checked = ref(false);

</script>

<style scoped>
.quiz {
  border-radius: 4px;
  background: #FFF;
  box-shadow: 0px 6px 12px 1px rgba(0, 0, 0, 0.06);
}

.nobg-btn {
  border: 1px solid #130204;
  /* Shadow/xs */
  border-radius: 8px;
  padding: 10px 18px;
  box-shadow: 0px 1px 2px 0px rgba(16, 24, 40, 0.05);
}
</style>