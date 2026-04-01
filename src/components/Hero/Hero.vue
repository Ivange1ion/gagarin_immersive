<script setup>
import Button from "../UI/Button.vue";
</script>

<template>
  <div class="container" id="hero">
    <h1 class="title">
      <span class="span">Гагарин</span> Иммерсив - космос начинается здесь
    </h1>
    <Button class="hero-btn"><a href="#about">Узнать больше</a></Button>
  </div>
</template>

<style scoped>
.container {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  /* margin-left: -30px;
  margin-right: -35px; */
  margin-top: -30px;
  margin-bottom: 30px;
  /* min-height: 200vh; */
  height: 150vh;
}

.container::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  opacity: 0.7;
  background-image: url("../../assets/img/hero-bg.webp");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  z-index: -1;
}

.title {
  color: var(--text);
  font-size: 67px;
  font-family: var(--sans);
  text-align: center;
  max-width: 915px;
  margin-top: 180px;
  margin-bottom: 88px;

  .span {
    color: var(--text-span);
  }
}

@media (max-width: 1200px) {
  .title {
    font-size: 57px;
  }
}

@media (max-width: 958px) {
  .title {
    font-size: 47px;
  }
}

@media (max-width: 720px) {
  .title {
    font-size: 37px;
  }
}

@media (max-width: 558px) {
  .container {
    height: 100vh;
  }
}
</style>
