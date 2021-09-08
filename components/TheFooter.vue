<template >
  <!-- Footer -->
  <div class=" row mt-a min-vw-100 bg-primary  pt-3 pb-5"  >
    <div class=" d-flex col-xl-12 col-lg-12 col-sm-12 col-12 pt-3 justify-content-center pb-5" style = "height : 300px">

      <div class="">
      <!-- Using v-if and v-else statements to change content -->
      <button v-on:click="sunny = !sunny">It's Sunny</button>
      <button v-on:click="cloudy = !cloudy">It's Cloudy</button>
      <p v-if="sunny">Sun! Yaay!</p>
      <p v-else-if="cloudy">Oh no, it's cloudy!</p>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
    // HomePage,
    // AccordionPage,
    // GridPage,
    // ImagePage
  },
  data() {
    return {
      sunny: false,
      cloudy: false
    }
  }
}
</script>

<style  scoped>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

</style>
