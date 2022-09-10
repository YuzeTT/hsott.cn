<script setup lang="ts">
const links: { name: string; icon?: string;icon_svg?: string;color: string; url: string }[] = [
  { name: 'Github', icon: 'i-carbon-logo-github', color: '', url: 'https://github.com/yuzett' },
  { name: 'Bilibili', icon_svg: 'M306.005333 117.632L444.330667 256h135.296l138.368-138.325333a42.666667 42.666667 0 0 1 60.373333 60.373333L700.330667 256H789.333333A149.333333 149.333333 0 0 1 938.666667 405.333333v341.333334a149.333333 149.333333 0 0 1-149.333334 149.333333h-554.666666A149.333333 149.333333 0 0 1 85.333333 746.666667v-341.333334A149.333333 149.333333 0 0 1 234.666667 256h88.96L245.632 177.962667a42.666667 42.666667 0 0 1 60.373333-60.373334zM789.333333 341.333333h-554.666666a64 64 0 0 0-63.701334 57.856L170.666667 405.333333v341.333334a64 64 0 0 0 57.856 63.701333L234.666667 810.666667h554.666666a64 64 0 0 0 63.701334-57.856L853.333333 746.666667v-341.333334A64 64 0 0 0 789.333333 341.333333zM341.333333 469.333333a42.666667 42.666667 0 0 1 42.666667 42.666667v85.333333a42.666667 42.666667 0 0 1-85.333333 0v-85.333333a42.666667 42.666667 0 0 1 42.666666-42.666667z m341.333334 0a42.666667 42.666667 0 0 1 42.666666 42.666667v85.333333a42.666667 42.666667 0 0 1-85.333333 0v-85.333333a42.666667 42.666667 0 0 1 42.666667-42.666667z', color: '#00AEEC', url: 'https://space.bilibili.com/1230104319' },
]
</script>

<template>
  <div my-6>
    <a v-for="(item, i) in links" :key="i" px-3 py-2 mt-2 mr-2 rounded-md bg-gray-50 inline-flex gap-2 hover:bg-gray-100 dark="bg-zinc-900 hover:bg-zinc-800" :href="item.url" target="_blank" transition-all>
      <div v-if="item.icon" :class="item.icon" text-xl />
      <div v-else-if="item.icon_svg">
        <svg w-6 h-6 t="1662830384682" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="2067" width="200" height="200"><path :d="item.icon_svg" p-id="2068" :fill="item.color" /></svg>
      </div>
      <div>{{ item.name }}</div>
    </a>
  </div>
</template>

<style scoped>

</style>
