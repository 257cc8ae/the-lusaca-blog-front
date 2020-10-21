<template>
  <div id="app">
    <AppHeader />
    <main>
      <router-view />
    </main>
  </div>
</template>

<script>
import AppHeader from "@/components/AppHeader.vue";

export default {
  name: "Home",
  components: {
    AppHeader,
  },
};
</script>

<style>
html,
body {
  margin: 0;
  background: #F7F7F7;
  font-family: "Inter", sans-serif;
}

main {
  width: 100%;
  max-width: 1020px;
  height: max-content;
  background: #ffffff;
  margin-right: auto;
  margin-left: auto;
  margin-top: 20px;
}
</style>
