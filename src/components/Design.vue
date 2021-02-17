<template>
  <div class="w-100">
    <div v-if="!ready" class="charging">
      <img
        src="../assets/circles-menu-1.gif"
        alt="Cargando..."
        class="image is-64x64"
      />
    </div>
    <div v-else>
      <div class="logo-container">
        <img src="../assets/Logo-dark.svg" alt="Logo IO" />
      </div>
      <section class="main-section">
        <p class="display-2 text-center">Design IO</p>
        <hr style="background-color: #202020" />
        <p class="text-justify">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sit labore
          molestias beatae ducimus porro fuga velit voluptatibus, sint sunt iure
          expedita dolorem dolorum ab iusto provident debitis molestiae error
          eaque. Lorem ipsum dolor sit amet consectetur adipisicing elit.
          Laboriosam impedit deleniti quam iusto dolore eius quibusdam
          distinctio dolorum a. Molestiae omnis modi repellendus, ad aliquid
          quos nisi ipsum laudantium inventore.
        </p>
      </section>
    </div>
  </div>
</template>
<script>
export default {
  name: "Design",
  data() {
    return {
      ready: false,
    };
  },
  mounted() {
    setTimeout(() => {
      this.ready = true;
    }, 2000);
  },
};
</script>
<style>
.charging {
  height: 100vh;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.logo-container {
  display: flex;
  justify-content: center;
  height: 100vh;
  width: 100%;
  align-items: center;
}

.logo-container > img {
  width: 50%;
  height: 50vh;
}

.main-section {
  padding: 3rem 14rem;
  background-color: #ffdb6c;
  color: #202020;
  border-radius: 0px 35px 0px 0px;
}
</style>
