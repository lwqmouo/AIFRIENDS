<script setup>

</script>

<template>
  <svg
    viewBox="0 0 24 24"
    width="24"
    height="24"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
  >
    <defs>
      <linearGradient id="orangeBlue" x1="0" y1="0" x2="1" y2="1">
        <stop offset="0%" stop-color="var(--brand-orange)" />
        <stop offset="100%" stop-color="var(--brand-blue)" />
      </linearGradient>
    </defs>

    <!-- 主用户 -->
    <circle
      cx="9"
      cy="8"
      r="3"
      stroke="url(#orangeBlue)"
      stroke-width="2"
    />
    <path
      d="M3 19c0-3.3 2.7-6 6-6s6 2.7 6 6"
      stroke="url(#orangeBlue)"
      stroke-width="2"
      stroke-linecap="round"
    />

    <!-- 副用户 -->
    <circle
      cx="17"
      cy="9"
      r="2"
      stroke="url(#orangeBlue)"
      stroke-width="2"
    />
    <path
      d="M15 19c.2-2 1.7-3.7 3.7-4"
      stroke="url(#orangeBlue)"
      stroke-width="2"
      stroke-linecap="round"
    />
  </svg>
</template>


<style scoped>
.friends-icon {
  animation: breathe 3s ease-in-out infinite;
}

@keyframes breathe {
  0%, 100% { opacity: 0.85 }
  50% { opacity: 1 }
}
</style>
