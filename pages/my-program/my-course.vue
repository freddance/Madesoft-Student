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


      <div class="bg-white px-4 py-4 mt-8">
        <div class="font-medium mt-2" style="font-size: 24px; color: #584143;">
          <div style="color: #FF4155;">Introduction to Industrial Automation</div>
        </div>

        <div class="mt-4">
          <img src="~assets/images/video.svg" class="" alt="">
        </div>

        <div class="mt-12">
          <div class="font-medium text-xl">What is Industrial Automation?</div>
          <p class="pt-2">Industrial Automation is the use of control devices such as computers, Programmable Logic
            Controllers (PLCs), Distributed Controllers (DCS), and Programmable Automation Controllers (PACs) to control industrial processes and machinery with the goal of removing as much human intervention as
            possible and replacing potentially dangerous assembly operations with automated operations.</p>

          <p class="pt-6">Before we engage fully in the theoretical details of what industrial automation is,
            let's take a look at the summary in the video <br> below.</p>
        </div>

        <div class="mt-8">
          <img src="~assets/images/video2.svg" class="" alt="">
        </div>

        <div style="background: #F5F5F5;" class="mt-10">
          <div class="grid grid-cols-3 px-6 py-10">
            <div class="col-span-2">
<!--              <img src="~assets/images/diagram.svg" class="" alt="">-->
            </div>

            <div class="pt-28">
              These diagram by the left depicts a typical case where things
              work with little or no human intervention, under the control of a PLC.
              This is a high-level pictorial view of a PLC dishing 1's and 0's to an industrial plant conveyor with a counter counting the packets as they pass through a sensor.
            </div>
          </div>
        </div>

        <div>
          <p class="mt-10">Specially designed hardware and software products are required for the
            automated system to be able to implement control and monitoring of industrial processes. </p>

          <p class="mt-4">In recent years, a growing number of such products have been developed by a
            growing number of vendors who specialize in the development of specialized software and hardware products for industrial automation and controls, among which are Siemens, ABB, Rockwell Automation, Emerson, Honeywell, Schneider Electric, Yokogawa,
            National Instruments, Omron, and other manufacturers are examples of such vendors. </p>
        </div>

      </div>

    </div>
  </div>
</template>


<script setup>

</script>

<style scoped>
.modules-border {
  border-radius: 8px;
  border: 1px solid #E7E7E7;
  background: #FDFDFD;
}

.faq_field {
  border-bottom: 1px solid #e7eaee;

}

.faq_field_wrapper {
  margin-top: 12px;
}

.invisible {
  visibility: hidden;
  opacity: 0;
  height: 0;
  transition: opacity 0.3s, height 0.3s, padding 0.3s, visibility 0.3s;
}

.visible {
  visibility: visible;
  height: auto;
  opacity: 1;
  padding: 10px 0px 10px;
  margin-bottom: 10px
}

.open_faq {
  cursor: pointer;
}

.rotate {
  transform: rotate(94deg);
}

.rotate-inner {
  transform: rotate(180deg);
}

.fa-angle-right {
  transition: transform 1s;
  color: black;
  padding-top: 38px;
}
</style>