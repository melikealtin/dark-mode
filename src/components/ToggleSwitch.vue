<template>
  <div class="toggle-wrapper">
    <label class="toggle">
      <input
        type="checkbox"
        :checked="mode === 'dark' ? 'checked' : false"
        @change="$emit('toggle')"
      />
      <span class="toggler round"></span>
    </label>
  </div>
</template>

<script>
export default {
  props: ["mode"],
};
</script>

<style lang="scss">
.toggle {
  position: relative;
  display: inline-block;
  width: 60px;
  height: 34px;
  input {
    opacity: 0;
    width: 0;
    height: 0;
    &:checked + .toggler {
      background: #2196f3;
      &:before {
        -webkit-transform: translateX(26px);
        -ms-transform: translateX(26px);
        transform: translateX(26px);
      }
    }
    &:focus + .toggler {
      box-shadow: 0 0 2px #2196f3;
    }
  }

  .toggler {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: #15202b;
    -webkit-transition: 0.4s;
    transition: 0.4s;
    &:before {
      position: absolute;
      content: "";
      height: 26px;
      width: 26px;
      left: 4px;
      bottom: 4px;
      background: #fff;
      -webkit-transition: 0.4s;
      transition: 0.4s;
    }
  }
  .toggler.round {
    border-radius: 34px;
    &:before {
      border-radius: 50%;
    }
  }
}
</style>
