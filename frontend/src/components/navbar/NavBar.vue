<script setup>

import MenuIcon from "@/components/navbar/icon/MenuIcon.vue";
import HomepageIcon from "@/components/navbar/icon/HomepageIcon.vue";
import FriendIcon from "@/components/navbar/icon/FriendIcon.vue";
import CreateIcon from "@/components/navbar/icon/CreateIcon.vue";
import SearchIcon from "@/components/navbar/icon/SearchIcon.vue";
import {useUserStore} from "@/stores/user.js";
import UserMenu from "@/components/navbar/UserMenu.vue";

const user = useUserStore();
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
      <div class="navbar-center w-3/4 max-w-150 flex justify-center">
        <div class="join w-3/4">
          <input class="input join-item rounded-l-full w-3/4" placeholder="Search For Friends" />
          <button class="btn join-item rounded-r-full gap-1">
            <SearchIcon/>
            o_O
          </button>
        </div>
      </div>
      <div class="navbar-end">
        <RouterLink v-if="user.isLogin()" :to="{name: 'create-index'}" active-class="btn-active" class="btn btn-ghost text-base mr-5">
          <CreateIcon/>
          Create
        </RouterLink>
        <RouterLink v-if="!user.isLogin()" :to="{name:'user-account-login-index'}" active-class="btn-active" class="btn btn-ghost mr-15 text-base">
          Log In
        </RouterLink>
        <UserMenu v-else/>
      </div>
    </nav>
    <!-- Page content here -->
    <slot>  </slot>
  </div>

  <div class="drawer-side is-drawer-close:overflow-visible">
    <label for="my-drawer-4" aria-label="close sidebar" class="drawer-overlay"></label>
    <div class="flex min-h-full flex-col items-start bg-base-200 is-drawer-close:w-16 is-drawer-open:w-64">
      <ul class="menu w-full grow">
        <li>
          <RouterLink :to="{name:'homepage-index'}" active-class="menu-focus" class="is-drawer-close:tooltip is-drawer-close:tooltip-right py-3" data-tip="首页">
            <HomepageIcon class="w-7 h-7" />
            <span class="is-drawer-close:hidden text-base ml-2 mt-1">Homepage</span>
          </RouterLink>
        </li>
        <li>
          <RouterLink :to="{name:'friend-index'}" active-class="menu-focus" class="is-drawer-close:tooltip is-drawer-close:tooltip-right py-3" data-tip="好友">
            <FriendIcon class="w-7 h-7" />
            <span class="is-drawer-close:hidden text-base ml-2 mt-1">Friends</span>
          </RouterLink>
        </li>
        <li>
          <RouterLink :to="{name:'create-index'}" active-class="menu-focus" class="is-drawer-close:tooltip is-drawer-close:tooltip-right py-3" data-tip="创作">
            <CreateIcon class="w-7 h-7" />
            <span class="is-drawer-close:hidden text-base ml-2 mt-1">Create</span>
          </RouterLink>
        </li>
      </ul>
    </div>
  </div>
</div>
</template>

<style scoped>

</style>