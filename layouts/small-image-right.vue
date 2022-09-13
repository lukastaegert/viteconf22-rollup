<template>
  <div class="grid grid-cols-[650px,1fr] w-full h-full">
    <div class="slidev-layout default">
      <slot/>
    </div>
    <div class="w-full h-full"
         :style="{backgroundImage: `linear-gradient(rgba(255, 255, 255, 0.333), rgba(255, 255, 255, 0.533)), url(${image})`}"
         style="color: white; background-repeat: no-repeat; background-position: center center; background-size: cover;"></div>
  </div>
</template>

<script setup>
const props = defineProps(['image'])
</script>