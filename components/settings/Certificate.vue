<template>
  <div class="px-10 mt-8">
    <div class="bg-white px-6 py-2">
      <h1 class="font-medium text-lg pt-4">Certificate</h1>

      <div>
        <h1 class="font-medium text-lg pt-8" style="color: #FF4155;">Great Job</h1>
        <p>You’ve earned your certificate</p>
      </div>
      <div class="grid grid-cols-2 gap-16">
        <div class="pt-8">
          <img src="~assets/images/certificate.svg" class="" alt="">
        </div>

        <div class="mt-12">
          <h1 class="font-medium">Share your course Certificate</h1>
          <p class="mt-4 text-sm">After you earn a course certificate, you can share it online on
            your LinkedIn profile or using a secured madesoftacademy URL</p>

          <p class="mt-4 text-sm">Made Soft does not provide a hard copy Certificates but you can download and print the Certificate PDF file</p>

          <input type="text"
                 class="input text-xs mt-8 block outline-none w-full p-4 "
                 placeholder="https://madesoft.com/certificate">

          <div>
            <MadesoftButton title="Share" class="w-40 mt-6"></MadesoftButton>
          </div>
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