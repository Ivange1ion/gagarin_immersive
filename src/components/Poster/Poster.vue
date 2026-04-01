<script setup></script>

<template>
  <section class="container" id="poster">
            <div class="part_head" style="margin-top: 0;">
            О проекте
        </div>
    <div style="display: flex; margin-bottom:40px">
      <picture class="poster-pic">
        <img src="../../assets/img/poster.webp" alt="" class="poster-img" />
      </picture>

      <div class="text-content center-aling">
        <p class="text-item">
          VR-проект «Полет Гагарина» — это не просто документальная реконструкция, 
          а полное физическое и эмоциональное погружение в событие, изменившее мир.
          </p>
      </div>
    </div>
    <p class="text-item">
                Вы окажетесь внутри легендарной капсулы «Восток-1», 
      услышите звуки старта и почувствуете те самые перегрузки при взлете. 
      Увидите своими глазами Землю из иллюминатора так, как её видел первый космонавт
        — хрупкую, огромную и завораживающе красивую.
      </p>
      <p class="text-item">
        Этот опыт позволяет шаг за шагом прожить легендарный полет 
        от первого лица, ощутив себя частью великой истории. 
        Наденьте шлем виртуальной реальности, чтобы сделать шаг из настоящего в бессмертный подвиг.
      </p>
  </section>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
}
.text-item{
  margin-top: 0;
  text-align: justify;
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
