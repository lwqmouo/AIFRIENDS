<script setup>
import UserMenu from "@/components/navbar/UserMenu.vue";
import {useUserStore} from "@/stores/user.js";
import UserSpaceIcon from "@/components/navbar/icon/UserSpaceIcon.vue";
import ProfileIndex from "@/views/user/profile/ProfileIndex.vue";
import UserProfileIcon from "@/components/navbar/icon/UserProfileIcon.vue";
import UserLogoutIcon from "@/components/navbar/icon/UserLogoutIcon.vue";

const user = useUserStore()

function closeMenu() {
  const element = document.activeElement
  if (element && element instanceof HTMLElement) element.blur()
}
</script>

<template>
  <div class="dropdown dropdown-end">
    <div tabindex="0" role="button" class="avatar btn btn-circle mr-6">
      <div class="w-8 rounded-full">
        <img :src="user.photo" alt="">
      </div>
    </div>
    <ul tabindex="-1" class="dropdown-content menu bg-base-100 rounded-box z-1 w-52 p-2 shadow-lg">
      <li>
        <RouterLink @click="closeMenu":to="{name: 'user-space-index',params: {user_id: user.id}}">
          <div class="avatar">
            <div class="w-10 rounded-full">
              <img :src="user.photo" alt="">
            </div>
          </div>
          <div class="text-base font-bold line-clamp-1 ml-2">{{user.username}}</div>
        </RouterLink>
      </li>
      <li>
        <RouterLink @click="closeMenu":to="{name: 'user-space-index',params: {user_id: user.id}}" class="text-sm font-bold py-3">
          <UserSpaceIcon />
          User Space
        </RouterLink>
      </li>
      <li>
        <RouterLink @click="closeMenu":to="{name: 'user-profile-index'}" class="text-sm font-bold py-3">
          <UserProfileIcon />
          User Profile
        </RouterLink>
      </li>
      <li></li>
      <li>
        <a @click="closeMenu"class="text-sm font-bold py-3">
          <UserLogoutIcon />
          Log Out
        </a>
      </li>
    </ul>
  </div>
</template>

<style scoped>

</style>