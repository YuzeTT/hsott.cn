<script setup lang="ts">
const router = useRouter()
const route = useRoute()
const links: { name: string; path?: string; url?: string; icon?: string }[] = [
  { name: '主页', path: '/' },
  { name: '项目', path: '/project' },
  { name: '关于', path: '/about' },
  { name: '', url: 'https://github.com/yuzett', icon: 'i-carbon-logo-github' },
]

const jump = (url?: string, path?: string) => {
  if (path)
    router.push(`${path}`)
  else
    window.open(url)
}
</script>

<template>
  <div text-xl flex justify-between items-center>
    <div text-2xl font-bold cursor-pointer @click="$router.push('/')">
      <div i-carbon-direction-loop-right />
    </div>
    <div flex gap-5 items-center>
      <div v-for="(item, i) in links" :key="i" transition-colors hover:text-zinc-800 font-bold :class="route.path === item.path ? 'text-zinc-800 dark:text-white cursor-default' : 'text-zinc-400 dark:text-zinc-500 cursor-pointer'" @click="jump(item.url, item.path)">
        <div v-if="item.icon" :class="item.icon" />
        <div>{{ item.name }}</div>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>
