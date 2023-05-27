<template>
  <header>
    <h1>{{ mode }}</h1>
    <toggle-switch :mode="mode" @toggle="$emit('toggle')"></toggle-switch>
    <nav>
      <div class="nav-link">Home</div>
      <div class="nav-link">About</div>
      <div class="nav-link">Portfolia</div>
      <div class="nav-link">Contact</div>
    </nav>
  </header>
</template>

<script>
import ToggleSwitch from "./ToggleSwitch.vue";
export default {
  components: { ToggleSwitch },
  props: ["mode"],
};
</script>

<style lang="scss">
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0px 25px;
  height: 60px;
  background: #c3c3c3;
  transition: background 0.3s ease-in-out;
  h1 {
    font-size: 32px;
    text-transform: uppercase;
    font-weight: 900;
  }
  nav {
    display: flex;
    height: 60px;
    .nav-link {
      display: flex;
      align-items: center;
      padding: 0px 15px;
      &:hover {
        background: #b0b0b0;
      }
    }
  }
}
.dark header {
  background: #15202b;
  nav {
    .nav-link {
      &:hover {
        background: #101520;
      }
    }
  }
}
</style>
