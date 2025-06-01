<template>
  <div class="app-container">
    <div class="sidebar-container">
      <Sidebar />
    </div>
    <div class="main-content">
      <router-view />
    </div>
  </div>
</template>

<script setup>
import Sidebar from './components/Sidebar.vue'
</script>

<style>
html,
body {
  margin: 0;
  padding: 0;
  height: 100%;
  box-sizing: border-box;
  font-family: "Segoe UI", sans-serif;
  overflow: hidden;
}

.app-container {
  display: flex;
  min-height: 100vh;
  background: #f4f4f4;
  overflow: hidden;
}

.sidebar-container {
  width: 260px;
  background: #ffffff;
  padding: 15px 0 15px 15px;
  border-radius: 20px;
  height: calc(100vh - 30px);
  margin: 15px 0 15px 15px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.04);
  position: sticky;
  top: 0;
}

.main-content {
  flex: 1;
  padding: 15px;
  background: #f4f4f4;
  height: 100vh;
  overflow-y: auto;
  scrollbar-width: none;
}

/* Optional: Hide scrollbar in WebKit (Chrome, Safari) */
.main-content::-webkit-scrollbar {
  display: none;
}

/* Responsive: stack layout for narrow screens */
@media (max-width: 768px) {
  .app-container {
    flex-direction: column;
  }

  .sidebar-container {
    width: 100%;
    height: auto;
    margin: 0;
    border-radius: 0;
    padding: 10px 15px;
  }

  .main-content {
    height: auto;
    padding: 10px;
  }
}
</style>
