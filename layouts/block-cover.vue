<script setup lang="ts">
defineProps<{ blockNum?: string }>()
</script>

<template>
  <div class="h-full flex overflow-hidden" style="padding-bottom: 48px">
    <!-- Blue left panel -->
    <div
      class="relative shrink-0 flex items-center justify-center overflow-hidden"
      style="width: 38%; background-color: #003c7d"
    >
      <!-- Large watermark number -->
      <span
        class="absolute font-black text-white select-none leading-none pointer-events-none"
        style="font-size: 20rem; opacity: 0.06; top: 50%; left: 50%; transform: translate(-50%, -48%)"
      >{{ blockNum }}</span>
      <!-- Foreground label -->
      <div class="relative z-10 text-center px-8">
        <div class="text-white font-semibold tracking-widest uppercase mb-3" style="font-size: 0.65rem; opacity: 0.5">
          Session Block
        </div>
        <div class="text-white font-black leading-none" style="font-size: 5.5rem">
          {{ blockNum }}
        </div>
      </div>
    </div>

    <!-- Content area -->
    <div class="flex-1 flex flex-col justify-center px-12 py-8 overflow-hidden">
      <slot />
    </div>
  </div>
</template>

<style scoped>
/* Heading inside the cover slide */
:deep(h1) {
  font-size: 1.85rem;
  font-weight: 800;
  color: #003c7d;
  line-height: 1.25;
  margin-bottom: 1.25rem;
}

/* Restyle the learning-objective green box into a blue left-accent card */
:deep(.border-green-400.bg-green-50) {
  background-color: #f0f5ff !important;
  border-color: transparent !important;
  border-left: 4px solid #003c7d !important;
  border-radius: 0 0.375rem 0.375rem 0 !important;
}
</style>
