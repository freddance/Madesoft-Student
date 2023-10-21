<template>
    <div>
  
  
      <div class="px-10 mt-8">
        <nuxt-link to="/schools/" class="flex px-2">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
            <path d="M10.875 19.3L4.27502 12.7C4.17502 12.6 4.10402 12.4917 4.06202 12.375C4.02002 12.2583 3.99935 12.1333 4.00002 12C4.00002 11.8667 4.02102 11.7417 4.06302 11.625C4.10502 11.5083 4.17568 11.4 4.27502 11.3L10.875 4.7C11.0583 4.51667 11.2877 4.421 11.563 4.413C11.8383 4.405 12.0757 4.50067 12.275 4.7C12.475 4.88333 12.5793 5.11267 12.588 5.388C12.5967 5.66333 12.5007 5.90067 12.3 6.1L7.40002 11H18.575C18.8583 11 19.096 11.096 19.288 11.288C19.48 11.48 19.5757 11.7173 19.575 12C19.575 12.2833 19.4793 12.521 19.288 12.713C19.0967 12.905 18.859 13.0007 18.575 13H7.40002L12.3 17.9C12.4833 18.0833 12.5793 18.3167 12.588 18.6C12.5967 18.8833 12.5007 19.1167 12.3 19.3C12.1167 19.5 11.8833 19.6 11.6 19.6C11.3167 19.6 11.075 19.5 10.875 19.3Z" fill="#FF4155"/>
          </svg>
          <span style="color: #FF4155;">Back</span>
        </nuxt-link>
  
  
        <div class="bg-white px-4 py-4 mt-8">
          <div class="flex gap-4 mt-2">
        
            <div class="font-medium flex" style="font-size: 24px; color: #584143;">
              <div style="color: #FF4155;">Module 1:</div> Fundamentals of Industrial Automation
            </div>
          </div>
  
          <div class="flex gap-4 mt-6">
            <div class="pt-12">
              
            </div>
  
  
            <div class="w-full gap-6 p-2 modules-border">
              <div class=" font-medium flex gap-8 cursor-pointer" @click="isOpen = !isOpen">
                  <div class="pt-1 flex gap-4">
                    <img src="~assets/images/Frame.svg" alt="">
                  </div>
                  <div class="text-xl pt-8">
                    Lesson 1.1: What is industrial Automation?
                  </div>
                <i class="fa fa-angle-right float-right flex justify-end ml-auto px-6" :class="isOpen ? 'rotate' : ''"></i>
              </div>
  
  
              <div class="invisible border-t" :class="isOpen ? 'visible mt-6' : ''">
                <div class="mx-32 mt-4">
                  <div class="flex cursor-pointer gap-2" @click="isOpenInner = !isOpenInner">
                    <i class="fa fa-angle-down px-2" :class="isOpenInner ? 'rotate-inner pt-1.5' : 'pt-1.5'"></i>
                    <span style="color: #FF4155;" class="font-medium text-lg">TOPICS</span>
                  </div>
  
                  <div class="invisible mx-10" :class="isOpenInner ? 'visible' : ''">
                    <nuxt-link to="/my-program/my-course" class="flex gap-6 mt-4" style="text-decoration: underline;"> <div>1:</div> <div>industrial Automation and Introduction to PLCs Programming</div> <div class="flex justify-end ml-auto"><i class="fa fa-check" aria-hidden="true"></i></div> </nuxt-link>
  
                    <nuxt-link to="/my-program/quiz" class="flex gap-6 mt-4" style="text-decoration: underline;">
                      <div class="pt-1">
                        <svg xmlns="http://www.w3.org/2000/svg" width="19" height="19" viewBox="0 0 19 19" fill="none">
                          <path d="M11.0835 11.8757C11.3078 11.8757 11.5026 11.7931 11.6677 11.6279C11.8329 11.4627 11.9153 11.2682 11.9147 11.0444C11.9147 10.8201 11.8322 10.6256 11.667 10.4609C11.5018 10.2963 11.3073 10.2137 11.0835 10.2132C10.8592 10.2132 10.6644 10.2958 10.4992 10.4609C10.3341 10.6261 10.2517 10.8206 10.2522 11.0444C10.2522 11.2687 10.3348 11.4635 10.5 11.6287C10.6652 11.7938 10.8597 11.8762 11.0835 11.8757ZM10.4897 9.34232H11.6772C11.6772 8.95968 11.7168 8.67917 11.796 8.50078C11.8752 8.32239 12.0599 8.08832 12.3502 7.79857C12.746 7.40274 13.0099 7.0829 13.1418 6.83907C13.2738 6.59524 13.3397 6.30813 13.3397 5.97774C13.3397 5.38399 13.1318 4.89922 12.7159 4.52344C12.3 4.14767 11.7559 3.95951 11.0835 3.95899C10.5425 3.95899 10.0707 4.11072 9.668 4.41419C9.2653 4.71767 8.98505 5.1201 8.82725 5.62149L9.896 6.0569C10.0147 5.72704 10.1765 5.47951 10.3813 5.31432C10.5861 5.14912 10.8201 5.06679 11.0835 5.06732C11.4002 5.06732 11.6575 5.15651 11.8554 5.3349C12.0533 5.51329 12.1522 5.75396 12.1522 6.0569C12.1522 6.24162 12.0995 6.41658 11.9939 6.58178C11.8884 6.74697 11.7036 6.95465 11.4397 7.20482C11.0043 7.58746 10.7373 7.8875 10.6386 8.10494C10.5399 8.32239 10.4903 8.73485 10.4897 9.34232ZM6.3335 14.2507C5.89808 14.2507 5.52521 14.0955 5.21487 13.7852C4.90454 13.4748 4.74964 13.1022 4.75016 12.6673V3.16732C4.75016 2.7319 4.90533 2.35903 5.21566 2.04869C5.526 1.73836 5.89861 1.58346 6.3335 1.58399H15.8335C16.2689 1.58399 16.6418 1.73915 16.9521 2.04949C17.2625 2.35982 17.4174 2.73243 17.4168 3.16732V12.6673C17.4168 13.1027 17.2617 13.4756 16.9513 13.7859C16.641 14.0963 16.2684 14.2512 15.8335 14.2507H6.3335ZM3.16683 17.4173C2.73141 17.4173 2.35854 17.2622 2.04821 16.9518C1.73787 16.6415 1.58297 16.2689 1.5835 15.834V4.75065H3.16683V15.834H14.2502V17.4173H3.16683Z" fill="#130204"/>
                        </svg>
                      </div>
                      <div>QUIZ</div>
                    </nuxt-link>
  
                    <div class="flex gap-6 mt-4" style="text-decoration: underline;">
                      <div class="pt-1">
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
                          <path d="M15.0334 17.4992C15.0001 18.8658 14.6668 21.0992 14.6668 21.0992L8.93345 21.1325L8.96678 19.1992C8.96678 19.1992 8.90012 15.4658 7.20012 14.0325C3.76678 11.1658 4.66678 5.13249 8.43345 3.63249C12.1668 2.13249 15.8668 3.23249 17.0001 4.89916C18.1334 6.56582 17.2001 7.96583 17.2001 7.96583C17.2001 7.96583 16.9334 8.46583 17.5668 9.49916C18.2001 10.5325 19.2001 12.9992 19.2001 12.9992L17.8334 13.4658C17.8334 13.4658 18.5001 16.6325 17.5668 17.0992C16.6334 17.5658 14.6668 17.3658 13.1668 16.8992" fill="#FCEA2B"/>
                          <path d="M19.7336 6.00065V11.234H14.9002C14.9002 11.234 12.0002 8.73398 14.9002 5.83398H19.7336V6.00065Z" fill="#9B9B9A"/>
                          <path d="M14.9334 7.33398H4.83341C4.83341 7.33398 4.16674 9.36732 4.83341 10.034H14.8667L14.9334 7.33398Z" fill="#9B9B9A"/>
                          <path d="M18.2666 5.86719H19.7999V11.3672H18.2666V5.86719Z" fill="black"/>
                          <path d="M18.467 11.2658C18.867 12.1658 19.2003 12.9992 19.2003 12.9992L17.8336 13.4658C17.8336 13.4658 18.5003 16.6325 17.567 17.0992C16.6336 17.5658 14.667 17.3658 13.167 16.9325M5.30029 7.33249C5.76696 5.66582 6.83363 4.23249 8.43363 3.63249C12.167 2.13249 15.867 3.23249 17.0003 4.89916C17.2336 5.23249 17.367 5.56582 17.467 5.86582" stroke="black" stroke-width="2" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"/>
                          <path d="M5.1001 10.032C5.26676 11.532 5.96676 12.9987 7.2001 14.032C8.9001 15.4654 8.96676 19.1987 8.96676 19.1987V21.132H14.7001C14.7001 21.132 15.0334 18.8654 15.0668 17.532M19.7334 5.9987V11.232H14.9001C14.9001 11.232 12.0001 8.73203 14.9001 5.83203H19.7334V5.9987Z" stroke="black" stroke-width="2" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"/>
                          <path d="M13.8667 7.33203H4.83341C4.83341 7.33203 4.16674 9.36536 4.83341 10.032H14.0001" stroke="black" stroke-width="2" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"/>
                          <path d="M18.2666 5.86523V11.1986" stroke="black" stroke-width="2" stroke-miterlimit="10"/>
                        </svg>
                      </div>
  
                      <div>VIRTUAL LAB</div>
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
  const isOpen = ref(false);
  const isOpenInner  = ref(false);
  const isOpenResources  = ref(false);
  const isOpenAssignment  = ref(false);
  
  
  const CreateModule = ref(false)
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