<template>
  <div class="slider" ref="slider">
    <div class="slider__controls">
      <a
        href="#"
        v-for="n in slides.length"
        :key="n"
        @click="moveSlider(n)"
        class="slider__controls__link"
        >{{ n }}</a
      >
    </div>
    <div
      v-for="(slide, index) in slides"
      :key="index"
      :style="`background-image:url(${slide.image})`"
      class="slider__content"
    >{{slide.text}}</div>
  </div>
</template>
<script>
export default {
  name: "AppSlider",
  data() {
    return {
      height: null,
      slider: null,
    };
  },
  mounted() {
    this.slider = this.$refs.slider;
    this.height = this.slider.offsetHeight;
  },
  props: {
    slides: {
      type: Array,
      required: true,
    },
  },
  methods: {
    moveSlider(n) {
      //n = n === 1 ? 0 : n;
      this.slider.scrollTo({
        top: this.height * (n-1),
        behavior: "smooth",
      });
    },
  },
};
</script>
<style>
::-webkit-scrollbar {
    display: none;
}
.slider {
  height: 100vh;
  background-color: #ccc;
  scroll-snap-type: y mandatory;
  overflow-y: scroll;
}

.slider__content {
  height: 100vh;
  background-position: center;
  background-size: cover;
  scroll-snap-align: center;
  scroll-snap-stop: normal;
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: calc(1.5rem + 4vmin);
}

.slider__controls {
  position: absolute;
  padding: 2em;
  top: 0;
  right: 0;
  width: 3rem;
  height: 100%;
  background-color: transparent;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.slider__controls__link {
  text-decoration: none;
  width: 3rem;
  height: 3rem;
  background-color: rgba(255, 255, 255, 0.8);
  color: black;
  display: flex;
  border-radius: 50%;
  justify-content: center;
  align-items: center;
  font-weight: bold;
  margin: 1rem 0;
}
</style>
