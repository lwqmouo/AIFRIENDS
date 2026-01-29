<script setup>
</script>

<template>
  <svg
    class="search-icon"
    width="24"
    height="24"
    viewBox="0 0 24 24"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
  >
    <defs>
      <linearGradient id="orangeBlue" x1="0" y1="0" x2="1" y2="1">
        <stop offset="0%" stop-color="var(--brand-orange)" />
        <stop offset="100%" stop-color="var(--brand-blue)" />
      </linearGradient>

      <!-- 轻微发光 -->
      <filter id="softGlow" x="-50%" y="-50%" width="200%" height="200%">
        <feGaussianBlur stdDeviation="1.5" result="blur" />
        <feMerge>
          <feMergeNode in="blur" />
          <feMergeNode in="SourceGraphic" />
        </feMerge>
      </filter>
    </defs>

    <!-- 放大镜圆 -->
    <circle
      class="lens"
      cx="11"
      cy="11"
      r="6"
      stroke="url(#orangeBlue)"
      stroke-width="2"
    />

    <!-- 手柄 -->
    <path
      class="handle"
      d="M16 16L21 21"
      stroke="url(#orangeBlue)"
      stroke-width="2"
      stroke-linecap="round"
    />
  </svg>
</template>

<style scoped>
.search-icon {
  cursor: pointer;
}

/* hover 只加“气质”，不改颜色 */
.search-icon:hover .lens,
.search-icon:hover .handle {
  filter: url(#softGlow);
}
</style>
