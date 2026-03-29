<script setup>
import { ref, watch } from "vue";
import useEmblaCarousel from "embla-carousel-vue";

const [emblaRef, emblaApi] = useEmblaCarousel();
const dataImg = [
  { id: 1, path: "assets/img/first-ach.webp" },
  { id: 2, path: "assets/img/second-ach.webp" },
  { id: 3, path: "assets/img/third-ach.webp" },
];

const prevButtonDisabled = ref(true);
const nextButtonDisabled = ref(true);

const toggleButtonsDisabled = (emblaApi) => {
  prevButtonDisabled.value = !emblaApi.canScrollPrev();
  nextButtonDisabled.value = !emblaApi.canScrollNext();
};

const goToPrev = () => emblaApi.value?.scrollPrev();
const goToNext = () => emblaApi.value?.scrollNext();

watch(
  emblaApi,
  (api) => {
    if (!api) return;

    toggleButtonsDisabled(api);
    api.on("reInit", toggleButtonsDisabled);
    api.on("select", toggleButtonsDisabled);
  },
  { immediate: true },
);
</script>

<template>
  <div class="embla">
    <div class="embla__viewport" ref="emblaRef">
      <div class="embla__container">
        <div v-for="img in dataImg" :key="img.id" class="embla__slide">
          <picture class="carusel-pic">
            <img class="carusel-img" :src="img.path" alt="" />
          </picture>
        </div>
      </div>
    </div>
    <div class="arrows">
      <button
        class="embla__prev"
        @click="goToPrev"
        :disabled="prevButtonDisabled"
      ></button>
      <button
        class="embla__next"
        @click="goToNext"
        :disabled="nextButtonDisabled"
      ></button>
    </div>
  </div>
</template>

<style scoped>
.embla {
  position: relative;
  overflow: hidden;
  width: 100%;
  --slide-gap: 1rem;
  --slide-count: 3;
}

.embla__viewport {
  overflow: hidden;
  width: 100%;
}

.embla__container {
  display: flex;
  gap: var(--slide-gap);
  backface-visibility: hidden;
  touch-action: pan-y pinch-zoom;
}

.embla__slide {
  display: flex;
  justify-content: center;
  align-items: center;
  flex: 0 0 100%;
  min-width: 0;
  max-width: 100%;
  /* width: 80%; */
  margin-bottom: 30px;
  transition:
    transform 0.2s ease,
    box-shadow 0.2s ease;
}

.embla__slide:not(:last-child) {
  margin-right: 16px;
}

.carusel-pic {
  display: flex;
  justify-content: center;
}

.carusel-img {
  transition: transform 0.3s ease;
  display: block;
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.arrows {
  display: flex;
  flex-direction: row;
  justify-content: center;
  margin-bottom: 30px;
  gap: 20px;
}
.embla__prev,
.embla__next {
  border: none;
  background-color: var(--text-span);
  height: 40px;
  width: 40px;
  border-radius: 16px;
  cursor: pointer;
}

.embla__prev {
  background-image: url("../../assets/img/arrow-active.webp");
  transform: rotate(180deg);
  background-size: contain;
}

.embla__prev:disabled {
  background-image: url("../../assets/img/arrow-disabled.webp");
  transform: rotate(0deg);
  background-size: contain;
}

.embla__next {
  background-image: url("../../assets/img/arrow-active.webp");
  background-size: contain;
}

.embla__next:disabled {
  background-image: url("../../assets/img/arrow-disabled.webp");
  transform: rotate(180deg);
  background-size: contain;
}
</style>
