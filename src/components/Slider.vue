<template>
  <div class="slider">
    <div class="contenedor">
      <div
        v-for="(slide, index) in slides"
        :key="index"
        :style="`background-image:url(${slide.image})`"
        class="child"
      >
      </div>
      <p>...</p>
    </div>
  </div>
</template>
<script>
export default {
  name: "Slider",
  props: {
    slides: {
      type: Array,
      required: true,
    },
  },
};
</script>
<style>
::-webkit-scrollbar {
  display: none;
}
.slider {
  width: 100%;
}
.contenedor {
  width: 100% !important;
  height: 100vh;
  scroll-snap-type: y mandatory;
  overflow-y: scroll;
}

.child {
  width: 100%;
  scroll-snap-align: center;
  height: 100vh;
  background-position: center;
  background-size: cover;

  scroll-snap-stop: end;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 12vmin;
  filter: blur(5px) brightness(40%);
}
</style>
