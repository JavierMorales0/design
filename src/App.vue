<template>
  <div id="app">
    <!--<NavBar />-->
    <transition
      enter-active-class="slideInLeft"
      leave-active-class="slideOutRight"
      mode="out-in"
    >
      <router-view />
    </transition>
  </div>
</template>
<script>
//import NavBar from "@/components/NavBar.vue";
export default {
  components: {
    //NavBar,
  }
};
</script>

<style lang="scss">
* {
  font-family: "Quicksand", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

html, body{
  margin: 0;
  padding: 0;
  max-width: 100%;
}



</style>
