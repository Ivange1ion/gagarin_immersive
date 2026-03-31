<script setup></script>

<template>
  <div id="footer">
    <div id="contacts">
      +7(922)-712-22-36
      <br />
      <br />
      gagarin.immersive@mail.ru
    </div>
    <div id="media-links">
      <img src="../../assets/img/Telegram.webp" alt="телеграмм" />
      <img src="../../assets/img/Vkontakte (VK).webp" alt="вконтакте" />
    </div>
  </div>
</template>

<style scoped>
#footer {
  background-color: var(--footer);
  height: 60px;
  display: flex;
  /* width: 100%; */
  justify-content: space-around;
  /* padding: 20px; */
  padding-left: 20px;
  padding-top: 20px;
  padding-bottom: 20px;
  margin-top: 40px;
}
#media-links {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
  margin-right: 20px;
}
#media-links img {
  width: 50px;
  height: 50px;
}
</style>
