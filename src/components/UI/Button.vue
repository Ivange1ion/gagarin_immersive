<script setup></script>

<template>
  <button class="btn"><slot></slot></button>
</template>

<style scoped>
.btn {
  background-color: #ff8d28;
  color: black;
  padding: 25px 250px;
  border-radius: 60px;
  text-align: center;
  font-size: 50px;
  cursor: pointer;
}

@media (max-width: 1200px) {
  .btn {
    font-size: 40px;
    padding-left: 200px;
    padding-right: 200px;
  }
}

@media (max-width: 958px) {
  .btn {
    font-size: 30px;
    padding-left: 150px;
    padding-right: 150px;
  }
}

@media (max-width: 720px) {
  .btn {
    font-size: 25px;
    padding-left: 110px;
    padding-right: 110px;
  }
}

@media (max-width: 558px) {
  .btn {
    font-size: 18px;
    padding-left: 90px;
    padding-right: 90px;
  }
}
</style>
