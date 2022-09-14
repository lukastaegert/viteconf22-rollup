<template>
  <div
    class="slidev-layout default grid justify-center content-center bg-cover bg-center"
    :style="style"
  >
    <slot />
  </div>
</template>

<script setup>
import { computed } from "vue";

const props = defineProps({
  background: { type: String },
});

const style = computed(
  () =>
    `color: white; background-image: linear-gradient(#0005, #0008),url('${
      import.meta.env.BASE_URL
    }${props.background}');`
);
</script>
