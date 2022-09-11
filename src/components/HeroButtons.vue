<script setup lang="ts">
const links: { name: string; icon?: string;color: string; url: string }[] = [
  { name: 'Github', icon: 'i-ri-github-fill', color: '', url: 'https://github.com/yuzett' },
  { name: 'Bilibili', icon: 'i-ri-bilibili-fill', color: '#00AEEC', url: 'https://space.bilibili.com/1230104319' },
]
</script>

<template>
  <div my-6>
    <a v-for="(item, i) in links" :key="i" h-10 px-3 mt-2 mr-2 rounded-md bg-zinc-50 inline-flex hover="bg-zinc-700 text-white" dark="bg-zinc-900 hover:bg-zinc-800" :href="item.url" target="_blank" transition-all items-center gap-2>
      <div :class="item.icon" text-xl h-10 />
      <div text-sm>{{ item.name }}</div>
    </a>
  </div>
</template>

<style scoped>

</style>
