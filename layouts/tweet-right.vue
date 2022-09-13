<template>
  <div class="slidev-layout default grid grid-cols-[1fr,550px] gap-5 w-full h-full content-center">
    <div class="justify-self-end self-center text-right">
      <slot/>
    </div>
    <div class="justify-self-start self-center w-3/4">
      <Tweet :id="tweet" v-if="tweetClick" v-click="1"/>
      <Tweet :id="tweet" v-else/>
    </div>
  </div>
</template>

<script setup>
defineProps(['tweet', 'tweetClick'])

const foo = '2';
</script>