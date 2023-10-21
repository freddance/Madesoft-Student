<template>
  <div class="px-10 mt-8">
    <div class="bg-white px-6 py-8">
      <h1 class="font-medium text-lg ">Change Password</h1>
      <p>Change your Made Soft password using the form below.</p>
      <div class="grid grid-cols-3 gap-14">
        <div class="col-span-2 pt-12">
          <div class="mt-2">
            <label>Old Password</label>
            <input type="text"
                   class="input text-xs mt-2 block outline-none w-full p-4 "
                   placeholder="Jonah">
          </div>

          <div class="mt-4">
            <label>New Password</label>
            <input type="text"
                   class="input text-xs mt-2 block outline-none w-full p-4 "
                   placeholder="austinejonah@gmail.com">
          </div>

          <div class="mt-4">
            <label>Retype Password</label>
            <input type="text"
                   class="input text-xs mt-2 block outline-none w-full p-4 "
                   placeholder="austinejonah@gmail.com">
          </div>




          <button class="black-button w-full w-60 mt-12">
            Update Password
          </button>
        </div>

        <div class="mt-12">

        </div>
      </div>
    </div>
  </div>
</template>


<script !src="">

</script>

<style>
.input {
  border-radius: 8px;
  border: 1px solid var(--neutral-100, #E7EAEE);
  background: #FBFBFB;
}
</style>