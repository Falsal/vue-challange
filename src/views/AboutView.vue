<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
  <div>
    <router-link to="/about/sample">Nested Page </router-link>
  </div>
  <router-view />
</template>

<script>
export default {
  name: "AboutView",
};
</script>
