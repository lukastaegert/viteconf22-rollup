<template>
  <div class="grid grid-cols-[650px,1fr] w-full h-full">
    <div class="slidev-layout default">
      <slot />
    </div>
    <div class="w-full h-full bg-cover bg-center" :style="style"></div>
  </div>
</template>

<script setup>
import { computed } from "vue";

const props = defineProps({
  image: { type: String },
});

const style = computed(
  () =>
    `background-image: linear-gradient(#fff5, #fff8),url('${
      import.meta.env.BASE_URL
    }${props.image}');`
);
</script>
