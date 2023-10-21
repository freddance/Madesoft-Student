<template>
  <div class="px-10">
      <div class="bg-white px-8 py-10">
        <div class="flex">
          <div class="flex gap-4">
            <img src="~assets/images/MaskGroup.svg" alt="" srcset="">
            <div class="">
              <h1 class="font-medium text-lg pt-0.5">David Adetoyi</h1>
              <p class="text-sm pt-1.5">Lorem ipsum dolor sit amet consectetur. <br>
                Diam justo aenean tortor urna odio.</p>
              <p class="text-sm pt-2">+2348012345768</p>
              <p class="text-sm">fredadebho@gmail.com</p>
              <div class="flex gap-4 pt-3">
                  <div class="text-sm" style="border-radius: 8px; background: #F3F7FF; padding: 6px 9px;">
                    Automation Egnr
                  </div>

                <div class="text-sm" style="border-radius: 8px; background: #F3F7FF; padding: 6px 9px;">
                  10 yrs Experience
                </div>
              </div>
            </div>
          </div>

          <div class="flex justify-end ml-auto">
            <button class="black-button w-full " @click="seek = true">
            <div class="flex gap-2">
              <svg xmlns="http://www.w3.org/2000/svg" class="pt-1" width="16" height="16" viewBox="0 0 16 16" fill="none">
                <path d="M8 3.33325V12.6666" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M3.33203 8H12.6654" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg> Seek Mentor Help
            </div>
            </button>
          </div>
        </div>

        <div class=" flex gap-x-20 mx-4 mt-16 cursor-pointer" >
          <div class="pb-4" @click="toggleType(OPTION_1)" :class="[type === OPTION_1 ? 'active' : 'text']">Experience</div>
          <div @click="toggleType(OPTION_2)" :class="[type === OPTION_2 ? 'active' : 'text']">About</div>
        </div>


        <div v-if="type === OPTION_1" class="mt-14 grid grid-cols-3">
          <div class="col-span-2">
            <div >
              <h1 class="font-medium">Experience</h1>

              <p class="pt-5 text-sm">Lorem ipsum dolor sit amet consectetur. Risus pellentesque enim adipiscing egestas amet nec non
                venenatis quisque. Quam sapien purus potenti in amet imperdiet nullam. Dolor fusce ultricies at nunc sed semper. Elit faucibus consectetur et amet amet. Vulputate suspendisse tellus vel leo dignissim bibendum gravida.
                Lorem scelerisque nec mi varius posuere viverra. Non nec nibh diam mauris eget pellentesque.</p>
            </div>

            <div class="pt-8">
              <h1 class="font-medium">My Specialties</h1>

              <p class="pt-4 text-sm font-medium" style="color: #FF4155;">
                1. Designing
              </p>
              <p class="text-sm">Programming.</p>
              <p class="text-sm">Configuration.</p>
              <p class="text-sm">Installation & Maintenance – ICSS, DCS, PLC.,</p>
              <p class="text-sm">HMI & Field Instrumentation.</p>
            </div>

            <div>


              <p class="pt-4 text-sm font-medium" style="color: #FF4155;">
                2. Software Development
              </p>
              <p class="text-sm">Windows and Web Application Design</p>
              <p class="text-sm">Development & Coding using the following Tech Stacks VueJS, PHP-Laravel, NodeJS, HTML, CSS & Javascripts. 3. Project Management</p>
            </div>
          </div>
        </div>

        <div v-if="type === OPTION_2" class="mt-14 grid grid-cols-3">
          <div class="col-span-2">
            <h1 class="font-medium">About Mentor</h1>

            <p class="pt-5 text-sm">I am a passionate Automation, Control & Software
              Specialist with 14Years+ industry based experience in Integrated Control and Safety Systems (ICSS). I have worked and have experience in Designing, Programming Installation & Deploying Integrated Control and Safety Systems (ICSS) with major Automation Original
              Equipment Manufacturers (OEMs) Devices, Products & Solutions.</p>

            <div class="flex mt-10 gap-2 cursor-pointer" @click="rate = true" style="border-radius: 8px; background: #FFFEEA; padding: 10px; width: 187px;">
              Rate your mentor
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <mask id="mask0_2633_9586" style="mask-type:luminance" maskUnits="userSpaceOnUse" x="1" y="1" width="22" height="22">
                <path d="M2.09339 11.0865C2.08205 10.9484 2.09798 10.8094 2.14017 10.6782C2.18236 10.5469 2.24989 10.4264 2.33847 10.3243C2.42705 10.2221 2.53475 10.1405 2.65473 10.0847C2.77472 10.0289 2.90437 10 3.03545 10H4.84155C5.0924 10 5.33298 10.1054 5.51036 10.2929C5.68774 10.4804 5.7874 10.7348 5.7874 11V20.5C5.7874 20.7652 5.68774 21.0196 5.51036 21.2071C5.33298 21.3946 5.0924 21.5 4.84155 21.5H3.8172C3.58046 21.5001 3.35232 21.4063 3.17781 21.2371C3.00331 21.068 2.89514 20.8358 2.87466 20.5865L2.09339 11.0865ZM8.62494 10.6875C8.62494 10.2695 8.87086 9.8955 9.22791 9.7175C10.0078 9.3285 11.3362 8.547 11.9354 7.4905C12.7077 6.1285 12.8533 3.668 12.877 3.1045C12.8803 3.0255 12.8784 2.9465 12.8883 2.8685C13.0165 1.892 14.799 3.0325 15.4823 4.2385C15.8536 4.8925 15.9009 5.752 15.8621 6.4235C15.82 7.1415 15.6209 7.835 15.4256 8.524L15.0094 9.9925H20.1439C20.2901 9.99249 20.4342 10.0283 20.5651 10.0971C20.6959 10.1658 20.8099 10.2658 20.8981 10.3889C20.9863 10.5121 21.0463 10.6553 21.0734 10.8071C21.1005 10.9589 21.094 11.1153 21.0543 11.264L18.5147 20.772C18.4587 20.9817 18.3393 21.1663 18.1749 21.2977C18.0105 21.4291 17.81 21.5001 17.6039 21.5H9.57078C9.31993 21.5 9.07935 21.3946 8.90197 21.2071C8.72459 21.0196 8.62494 20.7652 8.62494 20.5V10.6875Z" fill="#555555" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </mask>
              <g mask="url(#mask0_2633_9586)">
                <path d="M0 0H24V24H0V0Z" fill="#B09F00"/>
              </g>
            </svg>
            </div>
          </div>
        </div>
      </div>

    <Dialog v-model:visible="rate" modal header="" :dismissableMask="true" :closable="false" class="md:w-[50vw] w-96 ">
      <div class="mx-16">
        <h1 class="text-2xl font-semibold" style="color:  #323A46;">Rate your Mentor</h1>
        <p>What do you think of this mentor?</p>

        <div class="flex gap-5 mt-16">
          <div class="flex">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path d="M12 17.5C14.33 17.5 16.3 16.04 17.11 14H6.89C7.69 16.04 9.67 17.5 12 17.5ZM8.5 11C8.89782 11 9.27936 10.842 9.56066 10.5607C9.84196 10.2794 10 9.89782 10 9.5C10 9.10218 9.84196 8.72064 9.56066 8.43934C9.27936 8.15804 8.89782 8 8.5 8C8.10218 8 7.72064 8.15804 7.43934 8.43934C7.15804 8.72064 7 9.10218 7 9.5C7 9.89782 7.15804 10.2794 7.43934 10.5607C7.72064 10.842 8.10218 11 8.5 11ZM15.5 11C15.8978 11 16.2794 10.842 16.5607 10.5607C16.842 10.2794 17 9.89782 17 9.5C17 9.10218 16.842 8.72064 16.5607 8.43934C16.2794 8.15804 15.8978 8 15.5 8C15.1022 8 14.7206 8.15804 14.4393 8.43934C14.158 8.72064 14 9.10218 14 9.5C14 9.89782 14.158 10.2794 14.4393 10.5607C14.7206 10.842 15.1022 11 15.5 11ZM12 20C9.87827 20 7.84344 19.1571 6.34315 17.6569C4.84285 16.1566 4 14.1217 4 12C4 9.87827 4.84285 7.84344 6.34315 6.34315C7.84344 4.84285 9.87827 4 12 4C14.1217 4 16.1566 4.84285 17.6569 6.34315C19.1571 7.84344 20 9.87827 20 12C20 14.1217 19.1571 16.1566 17.6569 17.6569C16.1566 19.1571 14.1217 20 12 20ZM12 2C6.47 2 2 6.5 2 12C2 14.6522 3.05357 17.1957 4.92893 19.0711C5.85752 19.9997 6.95991 20.7362 8.17317 21.2388C9.38642 21.7413 10.6868 22 12 22C14.6522 22 17.1957 20.9464 19.0711 19.0711C20.9464 17.1957 22 14.6522 22 12C22 10.6868 21.7413 9.38642 21.2388 8.17317C20.7362 6.95991 19.9997 5.85752 19.0711 4.92893C18.1425 4.00035 17.0401 3.26375 15.8268 2.7612C14.6136 2.25866 13.3132 2 12 2Z" fill="black"/>
            </svg>
            <div>
              Excellent
            </div>
          </div>

          <div class="flex">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <g clip-path="url(#clip0_3469_3985)">
                <path d="M12 2C17.523 2 22 6.477 22 12C22 17.523 17.523 22 12 22C6.477 22 2 17.523 2 12C2 6.477 6.477 2 12 2ZM12 4C9.87827 4 7.84344 4.84285 6.34315 6.34315C4.84285 7.84344 4 9.87827 4 12C4 14.1217 4.84285 16.1566 6.34315 17.6569C7.84344 19.1571 9.87827 20 12 20C14.1217 20 16.1566 19.1571 17.6569 17.6569C19.1571 16.1566 20 14.1217 20 12C20 9.87827 19.1571 7.84344 17.6569 6.34315C16.1566 4.84285 14.1217 4 12 4ZM14.8 13.857C14.8933 13.7629 15.0044 13.6882 15.1268 13.6374C15.2492 13.5866 15.3804 13.5606 15.513 13.561C15.6455 13.5614 15.7766 13.5881 15.8987 13.6396C16.0208 13.6911 16.1315 13.7663 16.2243 13.8609C16.317 13.9556 16.3901 14.0677 16.4391 14.1908C16.4882 14.3139 16.5123 14.4455 16.5101 14.578C16.5078 14.7105 16.4792 14.8413 16.426 14.9626C16.3728 15.084 16.2959 15.1936 16.2 15.285C15.0794 16.3858 13.5708 17.0018 12 17C10.4292 17.0018 8.92064 16.3858 7.8 15.285C7.61503 15.0984 7.51093 14.8465 7.5102 14.5838C7.50948 14.321 7.61219 14.0685 7.79613 13.8809C7.98006 13.6933 8.23045 13.5856 8.49316 13.5811C8.75586 13.5767 9.00977 13.6758 9.2 13.857C9.94682 14.5912 10.9527 15.0018 12 15C13.09 15 14.077 14.565 14.8 13.857ZM8.5 8C8.89782 8 9.27936 8.15804 9.56066 8.43934C9.84196 8.72064 10 9.10218 10 9.5C10 9.89782 9.84196 10.2794 9.56066 10.5607C9.27936 10.842 8.89782 11 8.5 11C8.10218 11 7.72064 10.842 7.43934 10.5607C7.15804 10.2794 7 9.89782 7 9.5C7 9.10218 7.15804 8.72064 7.43934 8.43934C7.72064 8.15804 8.10218 8 8.5 8ZM15.5 8C15.8978 8 16.2794 8.15804 16.5607 8.43934C16.842 8.72064 17 9.10218 17 9.5C17 9.89782 16.842 10.2794 16.5607 10.5607C16.2794 10.842 15.8978 11 15.5 11C15.1022 11 14.7206 10.842 14.4393 10.5607C14.158 10.2794 14 9.89782 14 9.5C14 9.10218 14.158 8.72064 14.4393 8.43934C14.7206 8.15804 15.1022 8 15.5 8Z" fill="black"/>
              </g>
              <defs>
                <clipPath id="clip0_3469_3985">
                  <rect width="24" height="24" fill="white"/>
                </clipPath>
              </defs>
            </svg>
            <div>
              Good
            </div>
          </div>


          <div class="flex">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path d="M20 12C20 10.4177 19.5308 8.87103 18.6518 7.55544C17.7727 6.23984 16.5233 5.21447 15.0615 4.60896C13.5997 4.00346 11.9911 3.84504 10.4393 4.15372C8.88743 4.4624 7.46197 5.22433 6.34315 6.34315C5.22433 7.46197 4.4624 8.88743 4.15372 10.4393C3.84504 11.9911 4.00347 13.5997 4.60897 15.0615C5.21447 16.5233 6.23985 17.7727 7.55544 18.6518C8.87104 19.5308 10.4178 20 12 20C14.1217 20 16.1566 19.1571 17.6569 17.6569C19.1572 16.1566 20 14.1217 20 12ZM22 12C22 13.9778 21.4135 15.9112 20.3147 17.5557C19.2159 19.2002 17.6541 20.4819 15.8268 21.2388C13.9996 21.9957 11.9889 22.1937 10.0491 21.8079C8.10929 21.422 6.32746 20.4696 4.92894 19.0711C3.53041 17.6725 2.578 15.8907 2.19215 13.9509C1.8063 12.0111 2.00433 10.0004 2.76121 8.17317C3.51809 6.3459 4.79981 4.78412 6.4443 3.6853C8.08879 2.58649 10.0222 2 12 2C13.3132 2 14.6136 2.25866 15.8268 2.7612C17.0401 3.26375 18.1425 4.00035 19.0711 4.92893C19.9997 5.85752 20.7363 6.95991 21.2388 8.17317C21.7413 9.38642 22 10.6868 22 12ZM15.5 8C15.7967 8 16.0867 8.08797 16.3334 8.2528C16.58 8.41762 16.7723 8.65189 16.8858 8.92597C16.9994 9.20006 17.0291 9.50166 16.9712 9.79264C16.9133 10.0836 16.7704 10.3509 16.5607 10.5607C16.3509 10.7704 16.0836 10.9133 15.7926 10.9712C15.5017 11.0291 15.2001 10.9994 14.926 10.8858C14.6519 10.7723 14.4176 10.58 14.2528 10.3334C14.088 10.0867 14 9.79667 14 9.5C14.0101 9.10537 14.1714 8.72969 14.4506 8.45055C14.7297 8.17141 15.1054 8.01012 15.5 8ZM10 9.5C10 9.79667 9.91203 10.0867 9.74721 10.3334C9.58239 10.58 9.34812 10.7723 9.07403 10.8858C8.79994 10.9994 8.49834 11.0291 8.20737 10.9712C7.9164 10.9133 7.64912 10.7704 7.43934 10.5607C7.22957 10.3509 7.0867 10.0836 7.02883 9.79264C6.97095 9.50166 7.00065 9.20006 7.11418 8.92597C7.22772 8.65189 7.41998 8.41762 7.66665 8.2528C7.91332 8.08797 8.20333 8 8.5 8C8.89464 8.01012 9.27032 8.17141 9.54946 8.45055C9.8286 8.72969 9.98988 9.10537 10 9.5ZM17 15H13C12.2969 14.999 11.6059 15.1833 10.9967 15.5344C10.3875 15.8855 9.88158 16.3911 9.53 17L7.8 16C8.32694 15.0873 9.08497 14.3295 9.99782 13.8029C10.9107 13.2762 11.9461 12.9993 13 13H17V15Z" fill="black"/>
            </svg>

            <div>
              Fair
            </div>
          </div>

          <div class="flex">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path d="M7.57 20C6.23 20 5.14 18.91 5.14 17.57C5.14 16.5 6.32 14.5 7.57 12.81C8.82 14.5 10 16.5 10 17.57C10 17.8891 9.93715 18.2051 9.81503 18.4999C9.69291 18.7947 9.51392 19.0626 9.28827 19.2883C9.06262 19.5139 8.79474 19.6929 8.49992 19.815C8.2051 19.9371 7.88911 20 7.57 20ZM12 2C10.6868 2 9.38642 2.25866 8.17317 2.7612C6.95991 3.26375 5.85752 4.00035 4.92893 4.92893C3.05357 6.8043 2 9.34784 2 12C2 13.75 2.45 15.38 3.24 16.81C3.4 16 3.81 15.07 4.31 14.17C4.10357 13.4652 3.99918 12.7344 4 12C4 9.87827 4.84285 7.84344 6.34315 6.34315C7.84344 4.84285 9.87827 4 12 4C14.1217 4 16.1566 4.84285 17.6569 6.34315C19.1571 7.84344 20 9.87827 20 12C20 14.1217 19.1571 16.1566 17.6569 17.6569C16.1566 19.1571 14.1217 20 12 20C11.76 20 11.53 20 11.29 19.96C10.82 20.7 10.14 21.28 9.34 21.63C10.19 21.87 11.08 22 12 22C13.3132 22 14.6136 21.7413 15.8268 21.2388C17.0401 20.7362 18.1425 19.9997 19.0711 19.0711C19.9997 18.1425 20.7362 17.0401 21.2388 15.8268C21.7413 14.6136 22 13.3132 22 12C22 10.6868 21.7413 9.38642 21.2388 8.17317C20.7362 6.95991 19.9997 5.85752 19.0711 4.92893C18.1425 4.00035 17.0401 3.26375 15.8268 2.7612C14.6136 2.25866 13.3132 2 12 2ZM12 14C11.59 14 11.19 14.04 10.81 14.12C11.16 14.75 11.47 15.4 11.69 16H12C13.25 16 14.32 16.5 14.77 17.23L16.19 15.81C15.29 14.72 13.75 14 12 14ZM15.5 8C14.7 8 14 8.7 14 9.5C14 10.3 14.7 11 15.5 11C16.3 11 17 10.3 17 9.5C17 8.7 16.3 8 15.5 8ZM10 9.5C10 8.7 9.3 8 8.5 8C7.7 8 7 8.7 7 9.5C7 10.3 7.7 11 8.5 11C9.3 11 10 10.3 10 9.5Z" fill="black"/>
            </svg>

            <div>
              Poor
            </div>
          </div>


        </div>

        <div class="mt-10">
          <div class="font-medium" style="color: #130204;">Do you have any comment you will like to share?</div>
          <div class="p-4 text-sm mt-2" style="border-radius: 8px;border: 1px solid var(--neutral-100, #E7EAEE); background: #FBFBFB;">
            School of Engineering Technology focus on real job related hands on technical skill acquisition in Engineering
            with simultaneous exposure to the practice in the industry through project based training and mentorship by experience industry experts. Graduates are well prepared for the job in the specific field of study at graduation.
            MAT's School of Engineering offers technical and practical based certificate training in the following areas; Industrial Automation, Instrumentation, IOT, SCADA, HVAC, Electrical, Mechanical.
          </div>
        </div>

        <div class="font-medium mt-8" style="color: #130204;">May we follow you up on your comment?</div>
        <div class="flex mt-4 gap-4">
          <div class="flex align-items-center">
            <RadioButton v-model="ingredient" inputId="ingredient1" name="pizza" value="Yes" />
            <label for="ingredient1" class="ml-2">Yes</label>
          </div>

          <div class="flex align-items-center">
            <RadioButton v-model="ingredient" inputId="ingredient2" name="pizza" value="No" />
            <label for="ingredient1" class="ml-2">No</label>
          </div>
        </div>

        <div class="flex gap-6 mt-12">
          <div>
            <button class="cancel-button w-[200px]">Cancel</button>
          </div>
            <div>
              <MadesoftButton title="Send" class="w-[200px]"></MadesoftButton>
            </div>
        </div>
      </div>
    </Dialog>

    <Sidebar v-model:visible="seek" position="right" class="w-full ">
      <div class="mx-10">
        <h1 class="text-2xl"> <span class="font-semibold text-2xl">Seek Mentor Help</span> ( Engr Osas E.I )</h1>

        <div class="card flex justify-content-center mt-6">
          <Calendar v-model="date" inline showWeek />
        </div>

        <div class="mt-8">
          <div class="font-medium mb-2" style="color: #130204;">Meeting Duration</div>
          <Dropdown v-model="selectedCity" :options="cities" optionLabel="name" placeholder="1 hour" class="w-full md:w-14rem" />
        </div>

        <div class="font-medium mb-2 mt-8" style="color: #130204;">Choose Time</div>
        <div class=" grid grid-cols-3 gap-8">
          <div class="col-span-2">
            <div class="flex p-2 justify-between font-medium" style="background: #F9F9F9; color: #B6192A;">
              <div>9:00</div>
              <div>-</div>
              <div>9:00</div>
            </div>

            <div class="flex p-2 mt-4 justify-between font-medium" style="background: #F9F9F9; color: #B6192A;">
              <div>9:00</div>
              <div>-</div>
              <div>9:00</div>
            </div>
          </div>

          <div class="mt-12 mr-4">
            <MadesoftButton title="Next" @click="SeekHelp = true" class="w-[200px]"></MadesoftButton>
          </div>
        </div>

      </div>
    </Sidebar>

    <Sidebar v-model:visible="SeekHelp" position="right" class="w-full ">
      <div class="mx-10">
        <h1 class="text-2xl"> <span class="font-semibold text-2xl">Seek Mentor Help</span> ( Engr Osas E.I )</h1>


        <div class="flex gap-20 mt-10">
            <div>
              Duration: <span class="font-medium">1 HOUR</span>
            </div>

          <div>
            Time: <span class="font-medium"> 9:00am - 10:00am </span>
          </div>
        </div>

        <div class="mt-10">
          <div class="mt-4">
            <label>Add Title</label>
            <input type="text"
                   class="input text-xs mt-2 block outline-none w-full p-4 "
                   placeholder="austinejonah@gmail.com">
          </div>
        </div>


      </div>
    </Sidebar>
  </div>
</template>

<script setup>
import {useQueryParamsTabSwitch} from "~/composables/useSwitchQueryParams.js";

const rate = ref(false)
const seek = ref(false)
const SeekHelp = ref(false)

const date = ref();

const selectedCity = ref();
const cities = ref([
  { name: 'New York', code: 'NY' },
  { name: 'Rome', code: 'RM' },
  { name: 'London', code: 'LDN' },
  { name: 'Istanbul', code: 'IST' },
  { name: 'Paris', code: 'PRS' }
]);

let tabs = [
  'Experience',
  'About',
]

const type = useQueryParamsTabSwitch(tabs);
const OPTION_1 = tabs[0];
const OPTION_2 = tabs[1];

const toggleType = (_type) => {
  type.value = _type
}
</script>

<style scoped>
.active {
  border-bottom: 2px solid #FF4155;
  font-weight: 500;
}

.text {
  color: #584143;
}


.cancel-button {
    border-radius: 8px;
    font-size: 14px;
    height: 52px;
    padding: 1px 25px 1px;
  border: 1px solid #130204;
    box-shadow: 0px 1px 2px 0px rgba(16, 24, 40, 0.05);
  color: #130204;
}
</style>