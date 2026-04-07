<template>
  <footer
    class="bg-[#003c7d] absolute bottom-0 left-0 w-full flex items-center justify-between px-6 py-3 text-sm text-white z-20"
  >
    <!-- Left: logos -->
    <div class="flex items-center gap-4">
      <img
        src="/img/lumc-logo-blauw-engels.png"
        alt="LUMC"
        class="h-8 object-contain bg-white"
      />
      <img
        src="/img/Logo.png"
        alt="Coding Café"
        class="h-8 object-contain"
      />
    </div>

    <!-- Center: title -->
    <div class="text-center font-medium tracking-wide">
      LUMC DCC Coding Café - 7 April 2026
    </div>

    <!-- Right: slide numbers -->
    <div class="text-right tabular-nums">
      {{ $slidev.nav.currentPage }} / {{ $slidev.nav.total }}
    </div>
  </footer>
</template>
