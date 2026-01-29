<script setup>

</script>

<template>
  <svg viewBox="0 0 24 24" width="24" height="24" fill="none">
    <defs>
      <linearGradient id="ob" x1="0" y1="0" x2="1" y2="1">
        <stop offset="0%" stop-color="var(--brand-orange)" />
        <stop offset="100%" stop-color="var(--brand-blue)" />
      </linearGradient>
    </defs>

    <path
      d="M3 11.5L12 4l9 7.5"
      stroke="url(#ob)"
      stroke-width="2"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
    <path
      d="M6 10.5V20h12v-9.5"
      stroke="url(#ob)"
      stroke-width="2"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
  </svg>
</template>

<style>
.home-icon {
  transition: transform 0.25s ease;
}
.home-icon:hover {
  transform: translateY(-1px) scale(1.05);
}
</style>
