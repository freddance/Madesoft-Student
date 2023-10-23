<template>
  <div>
    <div class="bg-white px-10 py-4">
      <div class="flex">
        <h1 class="font-semibold head-text">Welcome back!</h1> <h1 class="head-text ml-2">Sharonace.</h1>
      </div>
      <p style="color: #8A8C8D;">27 August 2023</p>
    </div>

    <div class="mt-6 mx-10 bg-white" style="border-radius: 8px;">
      <div class=" p-4 grid grid-cols-5 gap-x-6">
        <div class="col-span-2">
          <div class="attendance p-4">
            <div class="flex justify-between">
              <div class="">
                <h1 class="text-xl text-medium">Time Spending</h1>
                <span>5h 45min</span>
              </div>
              <div>
                <Dropdown v-model="selectedCity" :options="cities" optionLabel="name" placeholder="Students" class="w-full md:w-14rem" />
              </div>
            </div>

            <div>

            </div>
          </div>
        </div>

        <div class="attendance p-5">
          <div class="flex justify-center mx-auto gap-4">
            <div>
              <img src="~assets/images/Hours.svg" alt="">
            </div>
            <div class="">
              <span class="font-xs">Hours Spent</span>
              <h1 class="text-xl font-medium">45</h1>
            </div>
          </div>

          <div class="flex justify-center mx-auto gap-4 mt-8">
            <div>
              <img src="~assets/images/Overall-Result.svg" alt="">
            </div>
            <div class="">
              <span class="font-xs">Overall Result</span>
              <h1 class="text-xl font-medium">360</h1>
            </div>
          </div>

          <div class="flex justify-center mx-auto gap-4 mt-8">
            <div>
              <img src="~assets/images/Completed.svg" class="" alt="">
            </div>
            <div class="mr-4">
              <span class="font-xs">Completed</span>
              <h1 class="text-xl font-medium ">15</h1>
            </div>
          </div>
        </div>

        <div class="col-span-2">
          <h1 class="font-medium text-lg">Upcoming Class</h1>
          <div class="attendance flex p-4 mt-14">
            <div class="time">
              9:00 am
            </div>
            <div class="text-sm ml-4">
              <h1>Introduction Industrial Automation</h1>
              <p style="color: #8A8C8D;" class="pt-1">Online <span class="ml-6">-</span>  <span class="ml-8"> Google meet</span></p>
            </div>
          </div>

          <div class="attendance flex p-4 mt-4">
            <div class="time">
              9:00 am
            </div>
            <div class="text-sm ml-4">
              <h1>Introduction Industrial Automation</h1>
              <p style="color: #8A8C8D;" class="pt-1">Online <span class="ml-6">-</span>  <span class="ml-8"> Google meet</span></p>
            </div>
          </div>
        </div>
      </div>


      <div class="grid p-4 grid-cols-2 mt-6 gap-6">
        <div>
          <h1 class="font-medium text-lg">Assignment Progress</h1>
          <div class="attendance flex p-4 mt-4">
            <div>
              <img src="~assets/images/Frame1171275450.svg" alt="">
            </div>
            <div class="text-sm ml-4">
              <h1>Industrial Automation and Introduction to PLCs Programming</h1>
              <p style="color: #8A8C8D;" class="pt-1">5 Assignment</p>
            </div>
            <div>
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20" fill="none">
                <path d="M7.74609 6.42253L11.3236 10L7.74609 13.5775L8.92443 14.7559L13.6803 10L8.92443 5.24419L7.74609 6.42253Z" fill="#C2C2C2"/>
              </svg>
            </div>
          </div>

          <div class="attendance flex p-4 mt-4">
            <div>
              <img src="~assets/images/Frame1171275450.svg" alt="">
            </div>
            <div class="text-sm ml-4">
              <h1>Industrial Automation and Introduction to PLCs Programming</h1>
              <p style="color: #8A8C8D;" class="pt-1">7 Assignment</p>
            </div>
            <div>
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20" fill="none">
                <path d="M7.74609 6.42253L11.3236 10L7.74609 13.5775L8.92443 14.7559L13.6803 10L8.92443 5.24419L7.74609 6.42253Z" fill="#C2C2C2"/>
              </svg>
            </div>
          </div>

          <div class="attendance flex p-4 mt-4">
            <div>
              <img src="~assets/images/Frame1171275450.svg" alt="">
            </div>
            <div class="text-sm ml-4">
              <h1>Industrial Automation and Introduction to PLCs Programming</h1>
              <p style="color: #8A8C8D;" class="pt-1">18 Assignment</p>
            </div>
            <div>
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20" fill="none">
                <path d="M7.74609 6.42253L11.3236 10L7.74609 13.5775L8.92443 14.7559L13.6803 10L8.92443 5.24419L7.74609 6.42253Z" fill="#C2C2C2"/>
              </svg>
            </div>
          </div>
        </div>

        <div>
          <h1 class="font-medium text-lg">Course Statistics</h1>
          <div class="attendance  ">
            <div class="flex p-9 mt-4">
              <div>
                <img src="~assets/images/fake-chart.svg" alt="">
              </div>

              <div class="flex justify-center mx-auto mt-2">
                <div>
                  <div class="flex ml-5 gap-3">
                    <div class="pt-1.5">
                      <svg xmlns="http://www.w3.org/2000/svg" width="15" height="15" viewBox="0 0 15 15" fill="none">
                        <circle cx="7.5" cy="7.5" r="7.5" fill="#C31162"/>
                      </svg>
                    </div>
                    <div>
                      <p style="color: #8A8C8D;" class="">Incomplete</p>
                      <h1 class="font-medium">20%</h1>
                    </div>
                  </div>

                  <div class="flex ml-5 gap-3 mt-5">
                    <div class="pt-1.5">
                      <svg xmlns="http://www.w3.org/2000/svg" width="15" height="15" viewBox="0 0 15 15" fill="none">
                        <circle cx="7.5" cy="7.5" r="7.5" fill="#0AA9CC"/>
                      </svg>
                    </div>
                    <div>
                      <p style="color: #8A8C8D;" class="">Completed</p>
                      <h1 class="font-medium">67%</h1>
                    </div>
                  </div>

                  <div class="flex ml-5 gap-3 mt-5">
                    <div class="pt-1.5">
                      <svg xmlns="http://www.w3.org/2000/svg" width="15" height="15" viewBox="0 0 15 15" fill="none">
                        <circle cx="7.5" cy="7.5" r="7.5" fill="#130204"/>
                      </svg>
                    </div>
                    <div>
                      <p style="color: #8A8C8D;" class="">In Progress</p>
                      <h1 class="font-medium">13%</h1>
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
</template>

<script setup>
</script>

<style>
.attendance {
  border-radius: 8px;
  background: var(--White, #FFF);
  box-shadow: 0px 0.4px 2px 0px rgba(16, 24, 40, 0.06), 0px 0.5px 3px 0px rgba(16, 24, 40, 0.10);
}

span{
  color: #626466;
  font-size: 14px;
}

.time {
  border-radius: 4px;
  background: #FFF;
  box-shadow: 0px 3px 6px 0px rgba(0, 0, 0, 0.09);
  padding: 11px 8px 12px 8px;
}
</style>