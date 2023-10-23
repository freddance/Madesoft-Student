<template>
  <div>
    <div class="grid grid-cols-2">
      <div>
        <img src="~assets/images/login-img.svg" style="height: 100vh;" alt="">
      </div>

      <div class=" mt-28 flex relative right-[90px] justify-center mx-auto">

        <div class="w-[590px]">
          <div class="bg-white py-6">
            <h1 class="font-bold head-text">Log In</h1>
            <p class="pt-2">Log in by entering your information below</p>
          </div>

          <div class="relative mb-4 mt-2 ">
            <label>email</label>
            <input type="text"
                   v-model="form.email"
                   class="input text-xs mt-2 block outline-none w-full p-4 "
                   placeholder="Current Password">
          </div>

          <div class="relative mb-1 ">
            <label>Password</label>
            <input type="text"
                   v-model="form.password"
                   class="input text-xs mt-2 block outline-none w-full p-4 "
                   placeholder="Current Password">
          </div>

          <div class="flex justify-between mt-8">
            <div class="">
              <Checkbox v-model="checked" :binary="true" /> <span class="ml-2" style="font-size: 14px;">Remember me</span>
            </div>

            <div style="font-size: 14px;" class="pt-1">
              Forget Password
            </div>
          </div>

          <nuxt-link to="/dashboard/">
            <MadesoftButton title="Login In" is-loading="" class="w-40 text-center justify-center mx-auto mt-16"></MadesoftButton>
          </nuxt-link>

        </div>


      </div>
    </div>
  </div>
</template>

<script setup>
import MadesoftButton from "~/components/MadesoftButton.vue";

definePageMeta({
  layout: "auth",
})


const checked = ref(false);

const form = [
  {
    password: '',
    email: ''
  }
]
</script>

<style scoped>

</style>