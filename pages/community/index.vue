<template>
  <div>

    <div class="bg-white px-10 py-6">
      <h1 class="font-bold head-text">Community</h1>
      <p>Connect with other here</p>
    </div>


    <div class=" px-10 mt-16">
      <div class="grid grid-cols-4 gap-4">
        <div class="p-4 bg-white px-6 py-8 text-center mt-6"  style="border-radius: 8px;">
          <button class="black-button">
            <div class="flex px-4 gap-2">
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
                <g clip-path="url(#clip0_2629_7865)">
                  <path d="M11.332 2.00004C11.5071 1.82494 11.715 1.68605 11.9438 1.59129C12.1725 1.49653 12.4177 1.44775 12.6654 1.44775C12.913 1.44775 13.1582 1.49653 13.387 1.59129C13.6157 1.68605 13.8236 1.82494 13.9987 2.00004C14.1738 2.17513 14.3127 2.383 14.4074 2.61178C14.5022 2.84055 14.551 3.08575 14.551 3.33337C14.551 3.58099 14.5022 3.82619 14.4074 4.05497C14.3127 4.28374 14.1738 4.49161 13.9987 4.66671L4.9987 13.6667L1.33203 14.6667L2.33203 11L11.332 2.00004Z" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                </g>
                <defs>
                  <clipPath id="clip0_2629_7865">
                    <rect width="16" height="16" fill="white"/>
                  </clipPath>
                </defs>
              </svg>
              Send Message
            </div>
          </button>

          <div class="mt-8 mx-4">
            <div class="flex gap-2 ">
              <div class="">
                <svg xmlns="http://www.w3.org/2000/svg" class="mt-1" width="16" height="16" viewBox="0 0 16 16" fill="none">
                  <path d="M5.14453 1.14282L5.14453 14.8571" stroke="#373737" stroke-width="1.14286" stroke-linecap="round"/>
                  <path d="M10.8555 1.14282L10.8555 14.8571" stroke="#373737" stroke-width="1.14286" stroke-linecap="round"/>
                  <path d="M14.8555 10.8572L1.14118 10.8572" stroke="#373737" stroke-width="1.14286" stroke-linecap="round"/>
                  <path d="M14.8555 6.28577L1.14118 6.28577" stroke="#373737" stroke-width="1.14286" stroke-linecap="round"/>
                </svg>
              </div>
              <div>
                Channels
              </div>
            </div>

            <div class="flex gap-2  mt-4">
              <div class="pt-1">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
                  <path d="M9.0026 4.00004V6.66671H10.6693M9.7926 1.33337H6.66927C6.31565 1.33337 5.97651 1.47385 5.72646 1.7239C5.47641 1.97395 5.33594 2.31309 5.33594 2.66671V10.6667C5.33594 11.0203 5.47641 11.3595 5.72646 11.6095C5.97651 11.8596 6.31565 12 6.66927 12H12.0026C12.3562 12 12.6954 11.8596 12.9454 11.6095C13.1955 11.3595 13.3359 11.0203 13.3359 10.6667V4.82804C13.3359 4.65041 13.3004 4.47458 13.2315 4.31087C13.1626 4.14716 13.0616 3.99887 12.9346 3.87471L10.7246 1.71337C10.4755 1.46981 10.141 1.33342 9.7926 1.33337Z" stroke="#373737" stroke-linecap="round" stroke-linejoin="round"/>
                  <path d="M10.668 12.0001V13.3334C10.668 13.687 10.5275 14.0262 10.2774 14.2762C10.0274 14.5263 9.68826 14.6667 9.33464 14.6667H4.0013C3.64768 14.6667 3.30854 14.5263 3.05849 14.2762C2.80844 14.0262 2.66797 13.687 2.66797 13.3334V6.00008C2.66797 5.64646 2.80844 5.30732 3.05849 5.05727C3.30854 4.80722 3.64768 4.66675 4.0013 4.66675H5.33464" stroke="#373737" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
              </div>
              <div>
                Drafts
              </div>
            </div>
            <ChartDropdown />
          </div>
        </div>

        <div class="col-span-3 ">
          <div>
            <div style="color: #494949;" class="font-medium">Chat with David Uzo</div>
            <div class="p-4 bg-white chart-box">
              <div class="grid grid-cols-2 mt-10 scroll">
                <div>
                  <div class="flex gap-2">
                    <img src="~assets/images/chart-img.svg" alt="">
                    <div>
                      <div class="left-chart">
                        Whatsup, David. Were you able to figure that assignment out?
                      </div>
                      <span>David Uzo</span>
                      <span class="ml-6" style="color: #BABABA; font-size: 12px">07:55am</span>
                    </div>
                  </div>
                </div>

                <div class=" justify-end gap-2 mt-28">
                  <div>
                    <div class="right-chart">
                      Lol, How far? I was about asking same,
                    </div>
                    <span class="" style="color: #BABABA; font-size: 12px">07:55am</span>
                  </div>
                </div>
              </div>

              <div class="flex mx-4 p-2 mt-10" style="border-radius: 4px; background: #F9F9F9;">
                <input type="text"
                       class=" text-xs  block outline-none w-full p-4 "
                       placeholder="austinejonah@gmail.com" style="background: #F9F9F9;">
                <button class="black-button">Send</button>
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

<style scoped>
.chart-box {
  border-radius: 8px;
  border: 1px solid #F2F2F2;
  background: #FFF;
}

.left-chart {
  border-radius: 20px 20px 20px 0px;
  background: #FFE6E6;
  padding: 10px 16px;
  color: #494949;
  font-size: 14px;
}

.right-chart {
  border-radius: 20px 20px 0px 20px;
  background: #F0F2FF;
  padding: 10px 16px;
}


.scroll {
  overflow-y: scroll;
  height: 400px;
}
</style>