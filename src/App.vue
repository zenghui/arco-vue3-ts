<script setup lang="ts">
// https://github.com/vueuse/head
// you can use this to manipulate the document head in any components,
// they will be rendered correctly in the html results with vite-ssg
useHead({
  title: 'Arco Vue3 template',
  meta: [
    { name: 'description', content: 'Arco Vue Starter Template' },
  ],
  link: [
    {
      rel: 'icon',
      type: 'image/svg+xml',
      href: '/favicon.svg',
    },
  ],
})

watchEffect(() => {
  if (isDark.value)
    document.documentElement.classList.add('dark')
  else
    document.documentElement.classList.remove('dark')
})
</script>

<template>
  <RouterView />
</template>
