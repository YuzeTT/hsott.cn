<script setup lang="ts">
const project: { name: string;text: string;emoji: string; url: string }[] = [
  { name: 'Blooock 起始页', text: '专为 Minecraft 玩家打造的起始页', emoji: '🥳', url: 'https://a.hsott.cn' },
  { name: 'UniAnalytics', text: '出站提示+数据统计', emoji: '📊', url: 'https://github.com/YuzeTT/UniAnalytics' },
]
</script>

<template>
  <div>
    <div text-2xl font-bold py-5>
      Project
    </div>
    <div grid grid-cols-1 sm:grid-cols-2 gap-5>
      <a v-for="(item, i) in project" :key="i" :href="item.url" target="_blank" bg-gray-50 p-5 rounded-md flex gap-5 justify-between items-center hover:bg-gray-100 transition-all dark="bg-zinc-900 hover:bg-zinc-800">
        <div>
          <div text-xl font-bold>
            {{ item.name }}
          </div>
          <div text-md mt-1 text-gray-400>
            {{ item.text }}
          </div>
        </div>
        <div text-5xl text-gray text-opacity-50 hover:text-opacity-100 transition-all>
          {{ item.emoji }}
        </div>
      </a>
    </div>
  </div>
</template>

<style scoped>

</style>
