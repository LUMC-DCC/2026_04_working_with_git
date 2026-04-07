<template>
  <div class="h-full flex flex-col overflow-hidden" style="padding-bottom: 48px">
    <!-- Top accent bar -->
    <div style="height: 5px; background-color: #003c7d; flex-shrink: 0" />

    <!-- Centered content area -->
    <div class="flex-1 flex items-center justify-center px-20">
      <slot />
    </div>
  </div>
</template>

<style scoped>
/* Strip the green box — let content breathe */
:deep(.border-green-400.bg-green-50) {
  border: none !important;
  background: transparent !important;
  padding: 0 !important;
  border-radius: 0 !important;
  width: 100%;
  max-width: 780px;
}

/* "Key takeaways — Block N" bold title */
:deep(.border-green-400.bg-green-50 > p:first-child strong),
:deep(.border-green-400.bg-green-50 > strong:first-child) {
  display: block;
  font-size: 1.6rem;
  font-weight: 800;
  color: #003c7d;
  margin-bottom: 1.25rem;
  padding-bottom: 0.75rem;
  border-bottom: 2px solid rgba(0, 60, 125, 0.15);
}

/* Bullet list */
:deep(.border-green-400.bg-green-50 ul) {
  list-style: none !important;
  padding: 0 !important;
  margin: 0 !important;
}

:deep(.border-green-400.bg-green-50 li) {
  padding: 0.4rem 0 0.4rem 1.75rem;
  position: relative;
  color: #1f2937;
  font-size: 1rem;
  line-height: 1.5;
}

:deep(.border-green-400.bg-green-50 li::before) {
  content: "→";
  position: absolute;
  left: 0;
  color: #003c7d;
  font-weight: 700;
}
</style>
