<script setup>

</script>

<template>
  <div class="flex justify-center mt-33" >
    <fieldset class="fieldset bg-base-200 border-base-300 rounded-box w-xs border p-4">
      <label class="label">Username</label>
      <input type="text" class="input" placeholder="Enter your username" />

      <label class="label">Password</label>
      <input type="password" class="input" placeholder="Enter your password" />

      <label class="label">Confirm Password</label>
      <input type="password" class="input" placeholder="Confirm your password" />

      <button class="btn btn-neutral mt-4">Sign up</button>
      <div class="flex justify-end">
        <RouterLink :to="{name:'user-account-login-index'}" class="btn btn-sm btn-ghost">
          Log in
        </RouterLink>
      </div>
    </fieldset>
  </div>
</template>

<style scoped>

</style>