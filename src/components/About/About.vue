<script setup></script>

<template>
  <div class="about" id="about">
    <div class="part_head">Мы - команда крутых специалистов</div>
    <div class="about_first">
      <img src="../../assets/img/denis.webp" id="denis" alt="" />
      <div class="text-item" id="text_first">
        Меня зовут Денис, и я являюсь основателем этой компании. <br /><br />
        Мы с командой создали замечательный проект, который поможет осуществить
        мечту писателей-фантастов и учёных - сделать космос доступнее для
        каждого.
      </div>
    </div>
    <div class="about_second text-item" id="text_second">
      <br />Проект получил несколько грантов и государственное спонсирование.
      <br /><br />
      Таким образом, Гагарин Иммерсив нацелен не только на техническое развитие
      виртуальной реальности, но и на духовное!
    </div>
  </div>
</template>

<style scoped>
.about_first {
  display: flex;
  flex-wrap: wrap;
  gap: 30px;
}
#text_first {
  width: 70%;
}
#text_second {
  width: auto;
}
#denis {
  width: 300px;
  height: 300px;
}
@media (max-width: 720px) {
  .text-item {
    font-size: 30px;
  }
}
@media (width<1152px) {
  #text_first {
    width: auto;
  }
}
</style>
