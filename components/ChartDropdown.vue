<template>
  <div class="faq_wrapper ">
    <div class="faq_field_wrapper">
      <div class="faq_field">
        <div class="open_faq" >
          <div class="title" style="font-size: 15px" @click="isOpen = !isOpen">
            <div class="flex gap-2 relative top-4">
              <div class="">
                <svg xmlns="http://www.w3.org/2000/svg" class="mt-1" width="16" height="16" viewBox="0 0 16 16" fill="none">
                  <path d="M5.14453 1.14282L5.14453 14.8571" stroke="#373737" stroke-width="1.14286" stroke-linecap="round"/>
                  <path d="M10.8555 1.14282L10.8555 14.8571" stroke="#373737" stroke-width="1.14286" stroke-linecap="round"/>
                  <path d="M14.8555 10.8572L1.14118 10.8572" stroke="#373737" stroke-width="1.14286" stroke-linecap="round"/>
                  <path d="M14.8555 6.28577L1.14118 6.28577" stroke="#373737" stroke-width="1.14286" stroke-linecap="round"/>
                </svg>
              </div>
              <div>
                Direct Messages
              </div>
            </div>
          </div>

          <div class="invisible mx-4 mt-6" style="font-size: 13px" :class="isOpen ? 'visible' : ''">
            <div class="flex">
              <img src="~assets/images/johan.svg" alt="">
              <div class="pt-2 ml-2">
                Austin Jonah
              </div>
            </div>
          </div>
        </div>


      </div>
    </div>
  </div>



</template>

<script setup>
import { ref } from "#imports";

// defineProps(["title", "subhead"]);

const isOpen = ref(false);


</script>



<style scoped>


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
  transform: rotate(180deg);
}

.fa-angle-down {
  transition: transform;
  color: black;
}
</style>