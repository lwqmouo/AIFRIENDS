<script setup>
import {useRoute, useRouter} from "vue-router";

const route = useRoute()
</script>

<template>
personal space:{{route.params.user_id}}
</template>

<style scoped>

</style>