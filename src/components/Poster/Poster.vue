<script setup></script>

<template>
  <section class="container" id="poster">
    <picture class="poster-pic">
      <img src="../../assets/img/poster.webp" alt="" class="poster-img" />
    </picture>

    <div class="text-content center-aling">
      <p class="text-item">Переживите первый полёт в космос!</p>
      <p class="text-item">
        Наш проект даёт возможность не просто посмотреть о первом полёте в
        космос, а очутиться там в виртуальной реальности.
      </p>
    </div>
  </section>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: row;
}

.poster-pic {
  display: flex;
  /* width: 545px; */
  height: 594px;
  margin-right: 70px;
}
.poster-img {
  width: 545px;
  object-fit: cover;
}

.text-content {
  align-items: center;
  justify-content: center;
}

@media (max-width: 1200px) {
  .text-item {
    font-size: 40px;
  }
}

@media (max-width: 958px) {
  .container {
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  .poster-pic {
    margin-right: 0;
    height: 494px;
  }
  .poster-img {
    width: 445px;
  }
}

@media (max-width: 720px) {
  .text-item {
    font-size: 30px;
  }
}

@media (max-width: 558px) {
  .poster-pic {
    height: 394px;
  }
  .poster-img {
    width: 345px;
  }
}
</style>
