<script setup>

import MenuIcon from "@/components/navbar/icon/MenuIcon.vue";
import HomepageIcon from "@/components/navbar/icon/HomepageIcon.vue";
import FriendIcon from "@/components/navbar/icon/FriendIcon.vue";
import CreateIcon from "@/components/navbar/icon/CreateIcon.vue";
import SearchIcon from "@/components/navbar/icon/SearchIcon.vue";
</script>

<template>
  <div class="drawer lg:drawer-open">
  <input id="my-drawer-4" type="checkbox" class="drawer-toggle" />
  <div class="drawer-content">
    <nav class="navbar w-full bg-base-300">
      <div class="navbar-start">
        <label for="my-drawer-4" aria-label="open sidebar" class="btn btn-square btn-ghost">
          <MenuIcon/>
        </label>
        <div class="px-0 font-bold text-xl">AI Friends</div>
      </div>
      <div class="navbar-center w-3/4 max-w-150">
        <div class="join w-3/4">
          <input class="input join-item rounded-l-full w-3/4" placeholder="Search For Friends" />
          <button class="btn join-item rounded-r-full gap-1">
            <SearchIcon/>
            o_O
          </button>
        </div>
      </div>
      <div class="navbar-end">
        <button class="btn btn-ghost mr-15 text-l">Log In </button>
      </div>
    </nav>
    <!-- Page content here -->
    <div class="p-4">Page Content</div>
  </div>

  <div class="drawer-side is-drawer-close:overflow-visible">
    <label for="my-drawer-4" aria-label="close sidebar" class="drawer-overlay"></label>
    <div class="flex min-h-full flex-col items-start bg-base-200 is-drawer-close:w-16 is-drawer-open:w-64">
      <!-- Sidebar content here -->
      <ul class="menu w-full grow">
        <!-- List item -->
        <li>
          <button class="is-drawer-close:tooltip is-drawer-close:tooltip-right py-3" data-tip="首页">
            <!-- Home icon -->
            <HomepageIcon class="w-7 h-7" />
            <span class="is-drawer-close:hidden text-base ml-2 mt-1">Homepage</span>
          </button>
        </li>
        <li>
          <button class="is-drawer-close:tooltip is-drawer-close:tooltip-right py-3" data-tip="好友">
            <!-- Home icon -->
            <FriendIcon class="w-7 h-7" />
            <span class="is-drawer-close:hidden text-base ml-2 mt-1">Friends</span>
          </button>
        </li>
        <li>
          <button class="is-drawer-close:tooltip is-drawer-close:tooltip-right py-3" data-tip="创作">
            <!-- Home icon -->
            <CreateIcon class="w-7 h-7" />
            <span class="is-drawer-close:hidden text-base ml-2 mt-1">Create</span>
          </button>
        </li>

      </ul>
    </div>
  </div>
</div>
</template>

<style scoped>

</style>