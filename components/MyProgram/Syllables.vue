<template>
  <div>
    <div class="px-10">
      <div class="flex px-2 mt-8">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
          <path d="M10.875 19.3L4.27502 12.7C4.17502 12.6 4.10402 12.4917 4.06202 12.375C4.02002 12.2583 3.99935 12.1333 4.00002 12C4.00002 11.8667 4.02102 11.7417 4.06302 11.625C4.10502 11.5083 4.17568 11.4 4.27502 11.3L10.875 4.7C11.0583 4.51667 11.2877 4.421 11.563 4.413C11.8383 4.405 12.0757 4.50067 12.275 4.7C12.475 4.88333 12.5793 5.11267 12.588 5.388C12.5967 5.66333 12.5007 5.90067 12.3 6.1L7.40002 11H18.575C18.8583 11 19.096 11.096 19.288 11.288C19.48 11.48 19.5757 11.7173 19.575 12C19.575 12.2833 19.4793 12.521 19.288 12.713C19.0967 12.905 18.859 13.0007 18.575 13H7.40002L12.3 17.9C12.4833 18.0833 12.5793 18.3167 12.588 18.6C12.5967 18.8833 12.5007 19.1167 12.3 19.3C12.1167 19.5 11.8833 19.6 11.6 19.6C11.3167 19.6 11.075 19.5 10.875 19.3Z" fill="#FF4155"/>
        </svg>
        <span style="color: #FF4155;">Back</span>
      </div>
    </div>

    <div class="px-10 mt-8">
      <div class="bg-white p-6" style="border-radius: 8px;">
        <div class="flex justify-between ">
          <div class="space-y-2">
            <h1 class="font-medium">Syllables</h1>
            <p >MAT CIAPP - Certificate in Industrial Automation and PLC Programming</p>
          </div>

          <div style="color: #207DFF;" class="space-y-4">
            7 Modules
            <div>
              1 Project
            </div>
          </div>
        </div>

        <div class="px-8 py-12 mt-12 syllables-inner ">
          <div class="border-b space-y-5 pb-8">
            <h1 class="font-medium"> <span style="color: #FF4155;">Module 1:</span> Fundamentals of Industrial</h1>
            <h1>Module Objectives: At the end of this module participants would have built strong understanding of Industrial Automation fundamentals.</h1>
            <h1>Lesson 1 - What is Industrial Automation </h1>
            <h1>Lesson 2 - Categories of Industrial Automation</h1>
            <h1 class="flex justify-between">Lesson 3 - Equipment’s used in Industrial Automation

              <nuxt-link to="#" style="color: #207DFF; text-decoration-line: underline;">
                Go to my Modules
              </nuxt-link>
            </h1>
          </div>

          <div class="border-b space-y-5 pb-8 pt-12">
            <h1 class="font-medium"> <span style="color: #FF4155;">Module 1:</span> Fundamentals of Industrial</h1>
            <h1>Module Objectives: At the end of this module participants would have built strong understanding of Industrial Automation fundamentals.</h1>
            <h1>Lesson 1 - What is Industrial Automation </h1>
            <h1>Lesson 2 - Categories of Industrial Automation</h1>
            <h1 class="flex justify-between">Lesson 3 - Equipment’s used in Industrial Automation

              <nuxt-link to="#" style="color: #207DFF; text-decoration-line: underline;">
                Go to my Modules
              </nuxt-link>
            </h1>
          </div>
        </div>
      </div>
    </div>
  </div>

</template>

<script setup>
</script>


<style>

.syllables-inner {
  border-radius: 20px;
  border: 1px solid #EFEFEF;
  background: #FFF;
  box-shadow: 0px 2px 9px -1px rgba(0, 0, 0, 0.09);
}
</style>