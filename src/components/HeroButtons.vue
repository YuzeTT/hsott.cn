<script setup lang="ts">
const links: { name: string; icon?: string;color: string; url: string }[] = [
  { name: 'Github', icon: 'i-carbon-logo-github', color: '', url: 'https://github.com/yuzett' },
  { name: 'Bilibili', color: '#00AEEC', url: 'https://space.bilibili.com/1230104319' },
]
</script>

<template>
  <div my-6>
    <a v-for="(item, i) in links" :key="i" h-10 px-3 py-2 mt-2 mr-2 rounded-md bg-gray-50 inline-flex hover:bg-gray-100 dark="bg-zinc-900 hover:bg-zinc-800" :href="item.url" target="_blank" transition-all items-center gap-2>
      <div v-if="item.icon" :class="item.icon" text-xl />
      <div v-else-if="item.name === 'Bilibili'">
        <BilibiliLogo />
      </div>
      <div text-sm>{{ item.name }}</div>
    </a>
  </div>
</template>

<style scoped>

</style>
