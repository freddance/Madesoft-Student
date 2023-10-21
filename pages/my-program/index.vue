<template>
    <div>
      <div class="bg-white px-10 py-4">
          <h1 class="font-semibold head-text">My Programs</h1>
        </div>


       <div class="px-10">
        <div class="grid grid-cols-1 mt-12 bg-white py-10 px-6" style="border-radius: 8px;" >
            <div class="flex flex-row program-card p-6 gap-10">
                <div>
                    <img src="~assets/images/SE.svg" alt="" srcset="">
                </div>

                <div>
                    <h1 class="font-semibold text-white text-2xl">MAT CIAPP - Certificate in Industrial Automation and PLC Programming</h1>

                    <div class="flex gap-8 mt-5 text-white border-b pb-4" style="">
                        <div style="border-radius: 100px; background: rgba(255, 255, 255, 0.05);padding: 10px 12px; ">
                            Electrical Engineering
                        </div>
                        <div class="pt-2.5 font-semibold">
                            23 Lessons
                        </div>
                        <div class="pt-2.5 font-semibold">
                            2 Assignments
                        </div>
                        <div class="pt-2.5 font-semibold">
                            1 Project
                        </div>
                    </div>

                    <div class="flex gap-x-20 mt-4 text-white " style="">
                        <div>
                            Start Date: 14 July 2023
                        </div>

                        <div>
                            Mentor: Engr Osas I.A
                        </div>
                    </div>

                    <div class="grid grid-cols-3">
                        <div class="col-span-2 pt-10">
                            <ProgressBar :value="50"></ProgressBar>
                        </div>
                        <nuxt-link to="/my-program/view-program" class="bg-white flex justify-end ml-auto" style="padding: 18px 25px; border-radius: 100px; width: 156px;">
                            View Program
                        </nuxt-link>
                    </div>
                </div>
            </div>

            <div class="text-center mt-10" style="color: #FF4155; text-decoration-line: underline;">
                Add More Programs
            </div>
        </div>
       </div>
  
      
    </div>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  .program-card {
    border-radius: 20px;
    border: 1px solid #FAFAFA;
    background: #0663A6;
    box-shadow: 0px 6px 9px 0px rgba(0, 0, 0, 0.10);
  }
  </style>