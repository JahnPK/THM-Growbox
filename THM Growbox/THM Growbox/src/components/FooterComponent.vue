<template>
  <footer class="footer">
    <div class="footer-links">
      <a href="#">Impressum</a>
      <a href="#">Datenschutzerklärung</a>
      <a href="#">Nutzungsbedingungen</a>
    </div>
    <p class="footer-text">&copy; 2024 THM Growbox. Alle Rechte vorbehalten.</p>
  </footer>
</template>

<script setup></script>

<style>
:root {
  --footer-bg: #4a5c66;
  --footer-text-color: #ffffff;
  --footer-link-color: #ffffff;
  --footer-link-hover: #80ba24;
  --footer-padding: 20px;
}

.footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: var(--footer-padding);
  background-color: var(--footer-bg);
  width: 100%;
}

.footer-links {
  display: flex;
  gap: 15px;
}

.footer-links a {
  color: var(--footer-link-color);
  text-decoration: none;
  font-size: 14px;
  transition: color 0.3s ease;
}

.footer-links a:hover {
  color: var(--footer-link-hover);
}

.footer-text {
  color: var(--footer-text-color);
  font-size: 14px;
}
</style>
