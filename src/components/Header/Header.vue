<script setup>
import { ref } from "vue";
import Modal from "../UI/Modal.vue";

const activeIndex = ref(0);
const isVisiable = ref(false);

const items = ref([
  { id: 1, name: "Главная" },
  { id: 2, name: "Проект" },
  { id: 3, name: "Команда" },
  { id: 4, name: "Достижения" },
  { id: 5, name: "Проекты" },
]);

const htmlClass = ref("");
const visiableOfBtn = ref({
  display: "flex",
});

const toggleVisiableOfBtn = () => {
  visiableOfBtn.value["display"] =
    visiableOfBtn.value["display"] === "flex" ? "none" : "flex";
};
const toggleModalMenu = () => {
  htmlClass.value = htmlClass.value === "active-hm" ? "" : "active-hm";
  isVisiable.value = !isVisiable.value;
  toggleVisiableOfBtn();
};
</script>

<template>
  <header class="container">
    <div class="content">
      <p
        v-for="(item, index) in items"
        :key="item.id"
        class="item"
        :class="{ active: activeIndex === index }"
        @click="activeIndex = index"
      >
        {{ item.name }}
      </p>
    </div>
    <button
      @click="toggleModalMenu"
      class="hamburger"
      :class="htmlClass"
      type="button"
      aria-label="Меню"
    >
      <span class="hamburger__box">
        <span class="hamburger__inner"></span>
      </span>
    </button>
    <slot v-if="isVisiable"></slot>
  </header>
</template>

<style scoped>
.container {
  position: absolute;
  z-index: 100;
  top: 0;
  left: 0;
  width: 100%;
  padding: 10px;
}

.content {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-around;
}

.item {
  color: var(--text);
  font-size: 30px;
  cursor: pointer;
  font-family: var(--sans);
  font-weight: 700;
}

.active {
  background-color: var(--bg-active);
  color: var(--text-span);
  text-align: center;
  padding: 15px 61px;
  border-radius: 34px;
}

.hamburger {
  display: none;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 40px;
  height: 40px;
  padding: 8px;
  background: transparent;
  border: none;
  cursor: pointer;
  transition: all 0.3s ease;
  z-index: 11000;
}

.hamburger__box {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 24px;
  height: 18px;
  position: relative;
}

.hamburger__inner {
  display: block;
  width: 24px;
  height: 2px;
  background: #fff;
  border-radius: 1px;
  transition: all 0.3s ease;
}

.hamburger__inner::before,
.hamburger__inner::after {
  content: "";
  position: absolute;
  left: 0;
  width: 24px;
  height: 2px;
  background: #fff;
  border-radius: 1px;
  transition: all 0.3s ease;
}

.hamburger__inner::before {
  top: 0;
  transform-origin: center;
}

.hamburger__inner::after {
  bottom: 0;
  transform-origin: center;
}

.hamburger.active-hm .hamburger__inner {
  background: transparent;
}

.hamburger.active-hm .hamburger__inner::before {
  transform: translateY(8px) rotate(45deg);
}

.hamburger.active-hm .hamburger__inner::after {
  transform: translateY(-8px) rotate(-45deg);
}

.hamburger--small {
  width: 32px;
  height: 32px;
}

.hamburger--small .hamburger__box {
  width: 20px;
  height: 15px;
}

.hamburger--small .hamburger__inner {
  width: 20px;
}

.hamburger--small .hamburger__inner::before,
.hamburger--small .hamburger__inner::after {
  width: 20px;
}

.hamburger--small.active-hm .hamburger__inner::before {
  transform: translateY(6.5px) rotate(45deg);
}

.hamburger--small.active-hm .hamburger__inner::after {
  transform: translateY(-6.5px) rotate(-45deg);
}

.hamburger--large {
  width: 48px;
  height: 48px;
}

.hamburger--large .hamburger__box {
  width: 28px;
  height: 21px;
}

.hamburger--large .hamburger__inner {
  width: 28px;
}

.hamburger--large .hamburger__inner::before,
.hamburger--large .hamburger__inner::after {
  width: 28px;
}

.hamburger--large.active-hm .hamburger__inner::before {
  transform: translateY(9.5px) rotate(45deg);
}

.hamburger--large.active-hm .hamburger__inner::after {
  transform: translateY(-9.5px) rotate(-45deg);
}
@media (max-width: 1200px) {
  .item {
    font-size: 20px;
  }
}

@media (max-width: 958px) {
  .active {
    padding: 8px 48px;
  }
}

@media (max-width: 720px) {
  .hamburger {
    display: flex;
  }
  .container {
    display: flex;
    justify-content: flex-end;
  }
  .content {
    display: none;
    align-items: flex-start;
  }
}
</style>
