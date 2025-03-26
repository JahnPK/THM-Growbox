<script setup>
import NavComponent from "./components/NavComponent.vue";
import SidebarComponent from "./components/SidebarComponent.vue";
import FooterComponent from "./components/FooterComponent.vue";
import MonitoringComponent from "./components/MonitoringComponent.vue";
</script>

<template>
  <NavComponent />
  <div class="container">
    <SidebarComponent />
    <MonitoringComponent />
  </div>
  <FooterComponent />
</template>

<style scoped>
.container {
  display: flex;
  flex: 1;
  height: calc(100vh - 60px - 40px); /* Full height minus navbar and footer height */
}
@media (max-width: 768px) {
  .container {
    flex-direction: column;
  }
  .sidebar {
    display: none; /* Hide the sidebar */
  }
}
</style>