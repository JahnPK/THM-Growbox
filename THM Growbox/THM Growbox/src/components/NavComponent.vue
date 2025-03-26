<template>
  <div class="navbar">
    <img
      src="/src/assets/logo-negativ.jpg"
      alt="THM Growbox Logo"
      class="logo"
    />
    <span>Dashboard</span>
    <div class="menu">
      <button class="menu-button">Digitaler Zwilling</button>
      <div class="menu-content">
        <a href="#">Growbox 1</a>
        <a href="#">Growbox 2</a>
        <a href="#">Growbox 3</a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.navbar {
  height: 60px;
  background-color: #4a5c66;
  color: white;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 20px;
  font-size: 20px;
}
.logo {
  height: 40px;
  margin-right: 10px;
}
.menu {
  position: relative;
  display: inline-block;
  font-size: 13px;
}
.menu-button {
  background-color: #4a5c66;
  color: white;
  border: none;
  cursor: pointer;
  font-size: 16px;
  padding: 10px;
}
.menu-content {
  display: none;
  position: absolute;
  right: 0;
  background-color: #4a5c66;
  box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
  z-index: 1;
}
.menu-content a {
  color: white;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}
.menu-content a:hover {
  background-color: #80ba24;
}
.menu:hover .menu-content {
  display: block;
}
</style>
