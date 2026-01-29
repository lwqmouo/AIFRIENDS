<script setup>

</script>

<template>
  <svg
    class="menu-icon"
    viewBox="0 0 64 64"
    width="32"
    height="32"
  >
    <defs>
      <linearGradient id="menuGrad" x1="0%" y1="0%" x2="100%" y2="100%">
        <stop offset="0%" stop-color="var(--brand-orange)" />
        <stop offset="100%" stop-color="var(--brand-blue)" />
      </linearGradient>
    </defs>

    <!-- 菜单线条 -->
    <rect x="12" y="18" width="40" height="4" rx="2" fill="url(#menuGrad)" />
    <rect x="12" y="30" width="40" height="4" rx="2" fill="url(#menuGrad)" />
    <rect x="12" y="42" width="40" height="4" rx="2" fill="url(#menuGrad)" />

    <!-- 纸飞机 -->
    <g class="plane">
      <path
        d="M44 8L60 4L52 22L46 16L44 8Z"
        fill="url(#menuGrad)"
      />
    </g>
  </svg>
</template>

<style>
.menu-icon {
  overflow: visible;
}

/* 初始：完全在画布外 */
.menu-icon .plane {
  opacity: 0;
  transform:
    translate(22px, -22px)
    rotate(-90deg)
    scale(0.4);
  transform-origin: center;
  transition:
    opacity 0.15s ease,
    transform 0.55s cubic-bezier(0.22, 1.4, 0.36, 1);
}

/* hover：飞入 + 回弹 */
.menu-icon:hover .plane {
  opacity: 1;
  transform:
    translate(-4px, 4px)
    rotate(8deg)
    scale(1.05);
}
</style>
