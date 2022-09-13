<template>
  <div
    class="slidev-layout default grid grid-cols-[1fr,550px] gap-5 w-full h-full content-center"
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
const props = defineProps({
  tweet: { type: String },
  tweetClick: { type: Boolean },
});
</script>
