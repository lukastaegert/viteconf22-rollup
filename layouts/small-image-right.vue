<template>
  <div class="grid grid-cols-[600px,1fr] w-full h-full">
    <div class="slidev-layout default">
      <slot/>
    </div>
    <div class="w-full h-full" style="color: white; background-image: url('https://source.unsplash.com/collection/94734566/1920x1080'); background-repeat: no-repeat; background-position: center center; background-size: cover;"></div>
  </div>
</template>

<script setup>
const props = defineProps(['image'])
</script>