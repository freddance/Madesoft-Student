<template>
  <div>

    <div class="bg-white px-10 py-6">
      <h1 class="font-bold head-text">Settings</h1>
      <p>Manage all your settings here</p>
    </div>


    <div class=" mt-8">
      <div class="px-10">

        <div class="overview-card py-3">
            <div>
              <div style="background: #FBFCFF; padding: 6px 12px;" class="flex gap-x-10 mx-4">
                <div class="cursor-pointer px-2" @click="toggleType(OPTION_1)" :class="[type === OPTION_1 ? 'active ' : 'text']">Personal Information</div>
                <div class="cursor-pointer px-2" @click="toggleType(OPTION_2)" :class="[type === OPTION_2 ? 'active ' : 'text']">Certificate</div>
                <div class="cursor-pointer px-2" @click="toggleType(OPTION_3)" :class="[type === OPTION_3 ? 'active ' : 'text']">Cards</div>
                <div class="cursor-pointer px-2" @click="toggleType(OPTION_4)" :class="[type === OPTION_4 ? 'active' : 'text']">Subscription & Billing History</div>
                <div class="cursor-pointer px-2" @click="toggleType(OPTION_5)" :class="[type === OPTION_5 ? 'active ' : 'text']">Password</div>
              </div>
            </div>
        </div>

      </div>

      <div  v-if="type === OPTION_1" class="pb-10 px-10">
        <SettingsPersonalInformation />
      </div>

      <div  v-if="type === OPTION_2">
          <SettingsCertificate  />
      </div>

      <div  v-if="type === OPTION_3">

      </div>

      <div  v-if="type === OPTION_4">
        <SettingsSubscriptionBilling />
      </div>

      <div  v-if="type === OPTION_5">
        <SettingsPassword />
      </div>


    </div>
  </div>
</template>


<script setup>
import {useQueryParamsTabSwitch} from "~/composables/useSwitchQueryParams";

let tabs = [
  'Overview',
  'All student',
  'Assessment',
  'Activities',
  'Payment History',
]

const type = useQueryParamsTabSwitch(tabs);
const OPTION_1 = tabs[0];
const OPTION_2 = tabs[1];
const OPTION_3 = tabs[3];
const OPTION_4 = tabs[4];
const OPTION_5 = tabs[5];

const toggleType = (_type) => {
  type.value = _type
}
</script>

<style scoped>
.overview-card {
  border-radius: 8px;
  background: var(--White, #FFF);
  box-shadow: 0px 1px 4px 0px rgba(16, 24, 40, 0.04), 0px 0.5px 3px 0px rgba(16, 24, 40, 0.04);
}

.active {
  color: #FF4155;
  border-radius: 4px;
  border: 1px solid #F8F8F8;
  background: var(--shades-white, #FFF);
  font-weight: 500;
  box-shadow: 0px 9px 6px -7px rgba(0, 0, 0, 0.09), 0px 0px 0px -1px rgba(0, 0, 0, 0.25);
}

.text {
  color: #584143; opacity: 0.5;
}
</style>