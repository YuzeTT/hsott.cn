<script setup lang="ts">
const props = defineProps({
  cn: String,
  en: String,
  icon: String,
  url: String,
})
</script>

<template>
  <div>
    <div font-bold py-5 flex justify-between items-center>
      <div>
        <div text-3xl>
          {{ props.cn }}
        </div>
        <div text-xl text-zinc-500>
          {{ props.en }}
        </div>
      </div>
      <a v-if="props.icon" text-3xl :class="icon" text-zinc-500 hover:text-zinc-800 target="_blank" :href="url" />
    </div>
  </div>
</template>

<style scoped>

</style>
