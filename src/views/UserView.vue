<template>
  <div>
    <h1>This user view {{ $route.params.id ?? "No id param available" }}</h1>
    <button @click="$router.push(`/user/${$route.params.id}/posts`)">
      user posts
    </button>
    <button @click="$router.push(`/user/${$route.params.id}/profile`)">
      user profile
    </button>

    <router-view></router-view>
  </div>
</template>

<script setup>
import { onMounted } from "vue";

// console.log("$route.query :>> ", $router.push());
onMounted(() => {
  // this.$router.push("df");
  console.log("Mounted");
});
console.log("Mounted2");
</script>

<style scoped></style>
