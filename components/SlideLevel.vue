<script setup lang="ts">
const props = defineProps<{ level: 1 | 2 | 3 }>()

const colors = {
  1: 'bg-green-500',
  2: 'bg-amber-400',
  3: 'bg-gray-400',
}

const color = colors[props.level]
</script>

<template>
  <div class="absolute top-4 right-6 flex gap-1">
    <div
      v-for="i in level"
      :key="i"
      class="w-3 h-3 rounded-full opacity-80"
      :class="color"
    />
  </div>
</template>
