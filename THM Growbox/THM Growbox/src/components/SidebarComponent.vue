<template>
  <div class="sidebar">
     <!--
    <button
      class="image-button"
      style="background-image: url('/src/assets/growbox.png')"
    ></button>
    <button
      class="image-button"
      style="background-image: url('/src/assets/digitaler-zwilling.png')"
    ></button>
    <button
      class="image-button"
      style="background-image: url('/src/assets/online-marketing.png')"
    ></button>
    -->
  </div>
</template>

<style scoped>
.sidebar {
  width: 100px;
  background-color: rgb(223, 223, 223);
  color: white;
  padding: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 10px;
  height: 100%; 
}
.image-button {
  width: 80px;
  height: 80px;
  padding-left: 20vw;
  background-size: cover;
  background-position: center;
  border: none;
  cursor: pointer;
  border-radius: 10px;
}
</style>