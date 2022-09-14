<template>
  <div
    class="slidev-layout default grid grid-cols-[1fr,550px] gap-5 w-full h-full content-center bg-cover bg-center"
    :style="style"
  >
    <div class="justify-self-end self-center text-right">
      <slot />
    </div>
    <div class="justify-self-start self-center w-3/4">
      <Tweet :id="props.tweet" v-if="props.tweetClick" v-click="1" />
      <Tweet :id="props.tweet" v-else />
    </div>
  </div>
</template>

<script setup>
import { computed } from "vue";

const props = defineProps({
  background: { type: String },
  tweet: { type: String },
  tweetClick: { type: Boolean },
});

const style = computed(
  () =>
    `color: white; background-image: linear-gradient(#0005, #0008),url('${
      import.meta.env.BASE_URL
    }${props.background}');`
);
</script>
