<script setup>
import { ref } from "vue";

const activeIndex = ref(0);

const items = ref([
  { id: 1, name: "Главная", link: "hero" },
  { id: 3, name: "Команда", link: "about" },
  { id: 4, name: "Достижения", link: "achiv" },
  { id: 5, name: "Проекты", link: "projects" },
]);
</script>

<template>
  <div class="container">
    <div class="content">
      <p
        v-for="(item, index) in items"
        :key="item.id"
        class="item"
        :class="{ active: activeIndex === index }"
        @click="activeIndex = index"
      >
        <a :href="`#${item.link}`">{{ item.name }}</a>
      </p>
    </div>
  </div>
</template>

<style scoped>
.container {
  display: none;
  justify-content: center;
  align-items: center;
  position: absolute;
}

.content {
  display: flex;
  flex-direction: column;
  gap: 10px;
  background-color: black;
  padding: 15px;
  border-radius: 16px;
  border: 1px solid rgb(255, 255, 255, 0.5);
  text-align: center;
  min-width: 302px;
}

.item {
  color: var(--text);
  font-size: 30px;
  cursor: pointer;
  font-family: var(--sans);
}

.active {
  background-color: var(--bg-active);
  color: var(--text-span);
  text-align: center;
  padding: 15px 61px;
  border-radius: 34px;
}

@media (max-width: 720px) {
  .container {
    display: flex;
  }

  .item {
    font-size: 25px;
  }
}
</style>
