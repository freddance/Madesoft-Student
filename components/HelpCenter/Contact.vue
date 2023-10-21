<template>
  <div class="px-10">
      <div class="bg-white px-6 py-12">
        <h1 class="font-medium text-lg pt-8">Send Message</h1>
       <div class="grid grid-cols-3 gap-14">
         <div class="col-span-2 pt-8">
           <div class="mt-2">
             <label>Your Name</label>
             <input type="text"
                    class="input text-xs mt-2 block outline-none w-full p-4 "
                    placeholder="Jonah">
           </div>

           <div class="mt-4">
             <label>Your Email</label>
             <input type="text"
                    class="input text-xs mt-2 block outline-none w-full p-4 "
                    placeholder="austinejonah@gmail.com">
           </div>

           <div class="mt-4">
             <label>Write a message</label>
             <div>
               <Textarea v-model="value" rows="5" class="input" cols="80" />
             </div>
           </div>

           <div class="flex mt-8">
             <svg xmlns="http://www.w3.org/2000/svg" class="mt-1" width="16" height="16" viewBox="0 0 16 16" fill="none">
               <g clip-path="url(#clip0_2655_11568)">
                 <path d="M6.66797 8.66672C6.95427 9.04948 7.31954 9.36618 7.739 9.59535C8.15846 9.82452 8.62231 9.9608 9.09907 9.99495C9.57583 10.0291 10.0544 9.9603 10.5022 9.79325C10.95 9.62619 11.3567 9.36477 11.6946 9.02672L13.6946 7.02672C14.3018 6.39805 14.6378 5.55604 14.6302 4.68205C14.6226 3.80806 14.2721 2.97202 13.654 2.354C13.036 1.73597 12.2 1.38541 11.326 1.37781C10.452 1.37022 9.60998 1.7062 8.9813 2.31339L7.83464 3.45339" stroke="#373737" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                 <path d="M9.33347 7.33332C9.04716 6.95057 8.68189 6.63387 8.26243 6.40469C7.84297 6.17552 7.37913 6.03924 6.90237 6.0051C6.4256 5.97095 5.94707 6.03974 5.49924 6.2068C5.0514 6.37386 4.64472 6.63527 4.3068 6.97332L2.3068 8.97332C1.69961 9.60199 1.36363 10.444 1.37122 11.318C1.37881 12.192 1.72938 13.028 2.3474 13.646C2.96543 14.2641 3.80147 14.6146 4.67546 14.6222C5.54945 14.6298 6.39146 14.2938 7.02013 13.6867L8.16013 12.5467" stroke="#373737" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
               </g>
               <defs>
                 <clipPath id="clip0_2655_11568">
                   <rect width="16" height="16" fill="white"/>
                 </clipPath>
               </defs>
             </svg>

             <div class="ml-2">Add attachment</div>
           </div>

           <button class="black-button w-full w-60 mt-12">
             Send Message
           </button>
         </div>

         <div class="mt-12">
          <div class="px-6 py-8" style="border-radius: 2px; background: #F5F8FF;">
            <h1 class="text-lg font-medium text-center pb-6" style="border-bottom: 1px solid #B8B8B9;">Contact Details</h1>

            <div class="flex gap-2 mt-12">
              <svg xmlns="http://www.w3.org/2000/svg" class="mt-1" width="16" height="16" viewBox="0 0 16 16" fill="none">
                <g clip-path="url(#clip0_2655_11577)">
                  <path d="M14.665 11.28V13.28C14.6657 13.4657 14.6277 13.6494 14.5533 13.8195C14.479 13.9897 14.3699 14.1424 14.233 14.2679C14.0962 14.3934 13.9347 14.489 13.7588 14.5485C13.5829 14.6079 13.3966 14.63 13.2117 14.6133C11.1602 14.3904 9.18966 13.6894 7.45833 12.5667C5.84755 11.5431 4.48189 10.1774 3.45833 8.56665C2.33165 6.82745 1.63049 4.84731 1.41166 2.78665C1.395 2.60229 1.41691 2.41649 1.47599 2.24107C1.53508 2.06564 1.63004 1.90444 1.75484 1.76773C1.87964 1.63102 2.03153 1.52179 2.20086 1.447C2.37018 1.37221 2.55322 1.33349 2.73833 1.33332H4.73833C5.06187 1.33013 5.37552 1.4447 5.62084 1.65567C5.86615 1.86664 6.02638 2.15961 6.07166 2.47998C6.15608 3.12003 6.31263 3.74847 6.53833 4.35332C6.62802 4.59193 6.64744 4.85126 6.59427 5.10057C6.5411 5.34988 6.41757 5.57872 6.23833 5.75998L5.39166 6.60665C6.3407 8.27568 7.72263 9.65761 9.39166 10.6067L10.2383 9.75998C10.4196 9.58074 10.6484 9.45722 10.8977 9.40405C11.1471 9.35088 11.4064 9.37029 11.645 9.45998C12.2498 9.68568 12.8783 9.84224 13.5183 9.92665C13.8422 9.97234 14.1379 10.1355 14.3494 10.385C14.5608 10.6345 14.6731 10.953 14.665 11.28Z" stroke="black" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                </g>
                <defs>
                  <clipPath id="clip0_2655_11577">
                    <rect width="16" height="16" fill="white"/>
                  </clipPath>
                </defs>
              </svg>
              <div>+234 (0) 81697403</div>
            </div>

            <div class="flex gap-2 mt-8">
              <svg xmlns="http://www.w3.org/2000/svg" class="mt-1" width="16" height="16" viewBox="0 0 16 16" fill="none">
                <path d="M2.66536 2.66675H13.332C14.0654 2.66675 14.6654 3.26675 14.6654 4.00008V12.0001C14.6654 12.7334 14.0654 13.3334 13.332 13.3334H2.66536C1.93203 13.3334 1.33203 12.7334 1.33203 12.0001V4.00008C1.33203 3.26675 1.93203 2.66675 2.66536 2.66675Z" stroke="black" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M14.6654 4L7.9987 8.66667L1.33203 4" stroke="black" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>

              <div>hello@madesoftacademy.com</div>
            </div>


            <div class="bg-white mt-16">
              <h1 class="text-md text-center pb-4 pt-4" style="color: #FF4155;">Available days for calls</h1>

              <p class="text-center">Monday - Thursday</p>
              <p  class="text-center text-xs" style="color: var(--656565, #656565);">(8:00am - 10:00pm)</p>

              <p class="text-center mt-8">Friday - Sunday</p>
              <p class="text-center text-xs pb-4" style="color: var(--656565, #656565);">8:00am - 5:00pm</p>
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
.input {
  border-radius: 8px;
  border: 1px solid var(--neutral-100, #E7EAEE);
  background: #FBFBFB;
}
</style>