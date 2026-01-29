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

    <circle
      cx="12"
      cy="12"
      r="9"
      stroke="url(#orangeBlue)"
      stroke-width="2"
    />
    <path
      d="M12 8v8M8 12h8"
      stroke="url(#orangeBlue)"
      stroke-width="2"
      stroke-linecap="round"
    />
  </svg>
</template>


<style scoped>
.menu li:hover .create-icon {
  transform: scale(1.1) rotate(3deg);
}

.menu li:active .create-icon {
  transform: scale(0.95);
}
</style>
