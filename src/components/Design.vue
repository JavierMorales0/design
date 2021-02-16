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
      <p>Cargado</p>
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
    height:100vh;
    width:100%;
    display:flex;
    justify-content:center;
    align-items:center
}
</style>
