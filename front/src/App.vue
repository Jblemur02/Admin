<script setup>
import SideNav from './components/SideNav.vue'
</script>

<template>
  <main>
    <SideNav id="nav" />
    <router-view id="content" />
  </main>
</template>

<style scoped>
main {
  display: flex;
  flex-direction: row;
  height: 100vh;
  justify-content: center;
  align-items: center;
}
#nav {
  width: 10%;
  padding: 0.5%;
}

#content {
  width: 90%;
  padding: 0.5%;
}
</style>
