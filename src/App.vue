<template>
  <RouterView />
</template>

<script setup>
import { RouterView } from 'vue-router'
import { onMounted } from 'vue'
import { useStorage } from '@vueuse/core'
import { useDark, useToggle } from '@vueuse/core'

const isDark = useDark()
const toggleDark = useToggle(isDark)

const state = useStorage('vueuse-color-scheme')

onMounted(() => {
  if (!state.value === 'light') {
    useDark()
  }
})
</script>
