<template>
  <div class="home">
    <h1>{{ message }}</h1>
  </div>
</template>

<style></style>
<script src="https://unpkg.com/@popperjs/core@2"></script>
<script>
import { createPopper } from "@popperjs/core";
// Popper.Defaults.modifiers.computeStyle.gpuAcceleration = false;

export default {
  mounted() {
    this.$nextTick(function () {
      var popper = new Popper(
        this.$refs["showInputButton"],
        this.$refs["dropdown"],
        {
          placement: "bottom-start",
        }
      );
      console.log(popper);
    });
  },
  data: function () {
    return {
      message: "Button Tester Page",
    };
  },
  created: function () {},
  methods: {},
};
</script>
