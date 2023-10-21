<template>
  <button class="w-full  black-button">{{title}}</button>
</template>


<script setup>
defineProps(
    {
      isLoading: {
        required: true
      },
      title: {
        required: true
      }
    }
)
</script>

<style >
.black-button{
  border-radius: 8px;
  background: #130204;
  color: white;
  font-size: 14px;
  height: 52px;
  padding: 1px 25px 1px;
  box-shadow: 0px 1px 2px 0px rgba(16, 24, 40, 0.05);
}
</style>