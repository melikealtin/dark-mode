<template>
  <div class="app" :class="mode">
    <header-section :mode="mode" @toggle="toggle"></header-section>
    <content-section :mode="mode"></content-section>
  </div>
</template>

<script>
import ContentSection from "./components/ContentSection.vue";
import HeaderSection from "./components/HeaderSection.vue";

export default {
  data() {
    return {
      mode: "light",
    };
  },
  components: {
    HeaderSection,
    ContentSection,
  },
  created() {
    window.addEventListener("keyup", this.keyPress);
  },
  methods: {
    keyPress(e) {
      if (e.key == "t") {
        this.toggle();
      }
    },
    toggle() {
      if (this.mode === "dark") {
        this.mode = "light";
      } else {
        this.mode = "dark";
      }
    },
  },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Roboto", sans-serif;
}

.app {
  width: 100vw;
  min-height: 100vh;
  background: #f3f3f3;
  color: #15202b;
  transition: background 0.3s ease-in-out;
}
.dark {
  background: #192734;
  color: #e8e8e8;
}
</style>
