<template>
  <div>
    <div class="bg-white px-10 py-4">
      <h1 class="font-semibold head-text">SAE - Assignment</h1>

      <div class="flex px-6 mt-8 mb-4">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
          <path d="M10.875 19.3L4.27502 12.7C4.17502 12.6 4.10402 12.4917 4.06202 12.375C4.02002 12.2583 3.99935 12.1333 4.00002 12C4.00002 11.8667 4.02102 11.7417 4.06302 11.625C4.10502 11.5083 4.17568 11.4 4.27502 11.3L10.875 4.7C11.0583 4.51667 11.2877 4.421 11.563 4.413C11.8383 4.405 12.0757 4.50067 12.275 4.7C12.475 4.88333 12.5793 5.11267 12.588 5.388C12.5967 5.66333 12.5007 5.90067 12.3 6.1L7.40002 11H18.575C18.8583 11 19.096 11.096 19.288 11.288C19.48 11.48 19.5757 11.7173 19.575 12C19.575 12.2833 19.4793 12.521 19.288 12.713C19.0967 12.905 18.859 13.0007 18.575 13H7.40002L12.3 17.9C12.4833 18.0833 12.5793 18.3167 12.588 18.6C12.5967 18.8833 12.5007 19.1167 12.3 19.3C12.1167 19.5 11.8833 19.6 11.6 19.6C11.3167 19.6 11.075 19.5 10.875 19.3Z" fill="#FF4155"/>
        </svg>
        <span style="color: #FF4155;">Back</span>
      </div>
    </div>




    <div class="px-16 mt-10">
      <div class="grid grid-cols-1 mt-12">
        <div class=" program-card ">
          <div class="flex flex-row p-8 gap-10">
            <div>
              <img src="~assets/images/Frame1171275497.svg" alt="" srcset="">
            </div>

            <div>
              <h1 class="font-medium text-black pt-1" style="font-size: 30px;">Introduction to Industrial Automation</h1>

              <div class="view flex w-32 justify-center mx-auto mt-12 gap-2">
                <svg xmlns="http://www.w3.org/2000/svg" width="17" height="16" viewBox="0 0 17 16" fill="none">
                  <path d="M9.16797 1.33337H4.5013C4.14768 1.33337 3.80854 1.47385 3.55849 1.7239C3.30844 1.97395 3.16797 2.31309 3.16797 2.66671V13.3334C3.16797 13.687 3.30844 14.0261 3.55849 14.2762C3.80854 14.5262 4.14768 14.6667 4.5013 14.6667H12.5013C12.8549 14.6667 13.1941 14.5262 13.4441 14.2762C13.6942 14.0261 13.8346 13.687 13.8346 13.3334V6.00004L9.16797 1.33337Z" stroke="#130204" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                  <path d="M9.16797 1.33337V6.00004H13.8346" stroke="#130204" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
                <div>
                  View
                </div>
              </div>

            </div>
          </div>

          <div class="border-t pt-2 px-8 py-4 justify-between flex">
            <div class="flex mt-2">
              <div style="border-radius: 4px; background: #EDEDED; padding: 3px 6px;">
                See Comments
              </div>
              <div class="ml-4 pt-0.5">
                Grade: <span style="color: #FF4155;">100%</span>
              </div>
            </div>

            <div class="flex gap-2 pt-2">
              <div class="pt-1.5">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
                  <g clip-path="url(#clip0_2785_19621)">
                    <path d="M7.9987 14.6667C11.6806 14.6667 14.6654 11.6819 14.6654 8.00004C14.6654 4.31814 11.6806 1.33337 7.9987 1.33337C4.3168 1.33337 1.33203 4.31814 1.33203 8.00004C1.33203 11.6819 4.3168 14.6667 7.9987 14.6667Z" stroke="#FF4155" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                    <path d="M8 10.6666H8.00667" stroke="#FF4155" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                    <path d="M8 5.33337V8.00004" stroke="#FF4155" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                  </g>
                  <defs>
                    <clipPath id="clip0_2785_19621">
                      <rect width="16" height="16" fill="white"/>
                    </clipPath>
                  </defs>
                </svg>
              </div>
              <div>
                Re-submit
              </div>
            </div>
          </div>
        </div>



      </div>
    </div>


  </div>
</template>

<script setup>
</script>

<style>
.program-card {
  border-radius: 20px;
  border: 1px solid #EFEFEF;
  background: #FFF;
  box-shadow: 0px 6px 9px 0px rgba(0, 0, 0, 0.09);
}

.view {
  border-radius: 4px;
  border: 1px solid #ECECEC;
  padding: 10px 18px;
  /* Shadow/xs */
  box-shadow: 0px 1px 2px 0px rgba(16, 24, 40, 0.05);
}
</style>