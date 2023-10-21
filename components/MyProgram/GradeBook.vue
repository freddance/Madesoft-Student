<template>
  <div>


    <div class="px-10 mt-8">
      <nuxt-link to="/schools/" class="flex px-6">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
          <path d="M10.875 19.3L4.27502 12.7C4.17502 12.6 4.10402 12.4917 4.06202 12.375C4.02002 12.2583 3.99935 12.1333 4.00002 12C4.00002 11.8667 4.02102 11.7417 4.06302 11.625C4.10502 11.5083 4.17568 11.4 4.27502 11.3L10.875 4.7C11.0583 4.51667 11.2877 4.421 11.563 4.413C11.8383 4.405 12.0757 4.50067 12.275 4.7C12.475 4.88333 12.5793 5.11267 12.588 5.388C12.5967 5.66333 12.5007 5.90067 12.3 6.1L7.40002 11H18.575C18.8583 11 19.096 11.096 19.288 11.288C19.48 11.48 19.5757 11.7173 19.575 12C19.575 12.2833 19.4793 12.521 19.288 12.713C19.0967 12.905 18.859 13.0007 18.575 13H7.40002L12.3 17.9C12.4833 18.0833 12.5793 18.3167 12.588 18.6C12.5967 18.8833 12.5007 19.1167 12.3 19.3C12.1167 19.5 11.8833 19.6 11.6 19.6C11.3167 19.6 11.075 19.5 10.875 19.3Z" fill="#FF4155"/>
        </svg>
        <span style="color: #FF4155;">Back</span>
      </nuxt-link>


      <div class="bg-white  mt-8" style="padding: 21px 28px 42px 29px; border-radius: 8px;">

          <div class=" flex gap-x-12 mx-4 mt-4 cursor-pointer" >
            <div class="pb-4" @click="toggleType(OPTION_1)" :class="[type === OPTION_1 ? 'active' : 'text']">Quizzes</div>
            <div @click="toggleType(OPTION_2)" :class="[type === OPTION_2 ? 'active' : 'text']">Assignments grades</div>
            <div @click="toggleType(OPTION_3)" :class="[type === OPTION_3 ? 'active' : 'text']">Lab work</div>
          </div>


        <div v-if="type === OPTION_1" class="mt-12">
          <div class="flex gap-4 mt-6">

            <div class="w-full gap-6 gradebook-border">
              <div class="flex justify-between" style="background: rgba(246, 245, 245, 0.30); padding: 21px 31px 18px 23px;">
                <div style="color: #FF4155;">
                  Module 1
                </div>

                <div >
                  Grade: <span style="color: #FF4155;">95%</span>
                </div>
              </div>


              <div >
                <div class=" flex gap-8 cursor-pointer" @click="isOpen = !isOpen" style="padding: 21px 31px 18px 23px;">
                  <div class="text-xl pt-8 flex gap-8">
                   <div class="font-medium"> Lesson 1.1:</div> What is industrial Automation?
                  </div>
                  <i class="fa fa-angle-right float-right flex justify-end ml-auto" :class="isOpen ? 'rotate' : ''"></i>
                </div>


                <div class="invisible border-t " :class="isOpen ? 'visible mt-6' : ''" style="padding: 21px 31px 18px 23px;">
                  <div class="pt-5">
                    <div class="flex cursor-pointer gap-4" @click="isOpenInner = !isOpenInner">
                      <i class="fa fa-angle-down px-2" :class="isOpenInner ? 'rotate-inner ' : 'pt-2'"></i>
                      <span style="color: #FF4155;" class=" text-lg">Topic Fundamentals of Industrial Automation</span>
                    </div>

                    <div class="invisible mx-10" :class="isOpenInner ? 'visible' : ''">
                      <div>
                        <div class="flex gap-4 mt-2">
                          <h1 class="font-medium">Q1:</h1>
                          <div>What is Industrial Automation</div>
                        </div>

                        <div class="answer flex justify-between gap-x-10 mt-4">
                          <div class="whitespace-nowrap font-medium">Your answer: </div>
                          <div>
                            This is a high-level pictorial view of a PLC dishing 1's
                            and 0's to an industrial plant conveyor with a counter counting the packets as they pass through a sensor.
                          </div>
                          <div>
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="25" viewBox="0 0 24 25" fill="none">
                              <g clip-path="url(#clip0_2895_21234)">
                                <path d="M22 11.5799V12.4999C21.9988 14.6563 21.3005 16.7545 20.0093 18.4817C18.7182 20.2088 16.9033 21.4723 14.8354 22.0838C12.7674 22.6952 10.5573 22.6218 8.53447 21.8744C6.51168 21.1271 4.78465 19.746 3.61096 17.9369C2.43727 16.1279 1.87979 13.9879 2.02168 11.8362C2.16356 9.68443 2.99721 7.63619 4.39828 5.99694C5.79935 4.35768 7.69279 3.21525 9.79619 2.74001C11.8996 2.26477 14.1003 2.4822 16.07 3.35986" stroke="#009621" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
                                <path d="M22 4.5L12 14.51L9 11.51" stroke="#009621" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
                              </g>
                              <defs>
                                <clipPath id="clip0_2895_21234">
                                  <rect width="24" height="24" fill="white" transform="translate(0 0.5)"/>
                                </clipPath>
                              </defs>
                            </svg>
                          </div>
                        </div>
                      </div>

                      <div class="mt-4">
                        <div class="flex gap-4 mt-2">
                          <h1 class="font-medium">Q2:</h1>
                          <div>What is Industrial Automation</div>
                        </div>

                        <div class="answer-failed flex justify-between gap-x-10 mt-4">
                          <div class="whitespace-nowrap font-medium">Your answer: </div>
                          <div>
                            This is a high-level pictorial view of a PLC dishing 1's
                            and 0's to an industrial plant conveyor with a counter counting the packets as they pass through a sensor.
                          </div>
                          <div>
                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="25" viewBox="0 0 24 25" fill="none">
                              <path d="M18 6.5L6 18.5" stroke="#C90303" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                              <path d="M6 6.5L18 18.5" stroke="#C90303" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                            </svg>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>

                </div>
              </div>


            </div>
          </div>
        </div>
      </div>

    </div>

    <Dialog v-model:visible="CreateModule" modal header="" :dismissableMask="true" :closable="false" class="md:w-[50vw] w-96 ">
      <SchoolModalCreateModule />
    </Dialog>
  </div>
</template>


<script setup>
import {  Menu, MenuButton, MenuItem, MenuItems } from '@headlessui/vue'
import {useQueryParamsTabSwitch} from "~/composables/useSwitchQueryParams.js";
const isOpen = ref(false);
const isOpenInner  = ref(false);

let tabs = [
  'Quizzes',
  'Assignments grades',
  'Lab work',
]

const type = useQueryParamsTabSwitch(tabs);
const OPTION_1 = tabs[0];
const OPTION_2 = tabs[1];
const OPTION_3 = tabs[3];

const toggleType = (_type) => {
  type.value = _type
}

const CreateModule = ref(false)
</script>

<style scoped>
.gradebook-border {
  border-radius: 20px;
  border: 1px solid #EFEFEF;
  background: #FFF;
}

.faq_field {
  border-bottom: 1px solid #e7eaee;

}

.text{
  color: #584143;
  opacity: 0.5;
}

.active {
  border-bottom: 2px solid #FF4155;
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
  margin-bottom: 10px;
}

.open_faq {
  cursor: pointer;
}

.rotate {
  transform: rotate(94deg);
}

.rotate-inner {
  transform: rotate(180deg);
  position: relative;
  bottom: 3px;
}

.fa-angle-right {
  transition: transform 1s;
  color: black;
  padding-top: 38px;

}

.answer {
  border-radius: 4px;
  background: rgba(206, 250, 169, 0.10);
  padding: 12px;
  color: #009621;
  font-size: 12px;
}

.answer-failed {
  padding: 12px;
  color: #C90303;
  font-size: 12px;
  border-radius: 4px;
  background: rgba(255, 65, 85, 0.05);
}
</style>