<template>
  <div class="grid grid-cols-[650px,1fr] w-full h-full">
    <div class="slidev-layout default">
      <slot />
    </div>
    <div
      class="w-full h-full"
      :style="{
        backgroundImage: `linear-gradient(#fff5, #fff8), url(${props.image})`,
      }"
      style="background-position: center center; background-size: cover"
    ></div>
  </div>
</template>

<script setup>
const props = defineProps({
  image: { type: String },
});
</script>
