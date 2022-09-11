<template>
  <main font-sans p="x-4 y-10" text="gray-700 dark:gray-200">
    <div class="px-6 xl:text-lg dark:prose-invert">
      <Navbar />
    </div>
    <Framework>
      <router-view />
      <Footer />
    </Framework>
  </main>
</template>
