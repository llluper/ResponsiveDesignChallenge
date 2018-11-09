<template>
  <button class="buttonn">
    {{ text }}
    <div class="plus-out">
      <span class="plus"></span>
    </div>
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    text: String,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_variables.scss";
.buttonn {
  background-color: transparent;
  padding: 0 0 0 20px;
  position: relative;
  display: inline-block;
  border-radius: 0;
  border: 1px solid $primary-orange;
  border-right: none;
  color: $primary-blue;
  height: 40px;
  width: 170px;
  line-height: 40px;
  font-family: 'Muli', sans-serif;
  font-size: 10px;
  font-weight: 900;
  letter-spacing: 1.17px;
  text-align: left;
  &:hover {
    color: $primary-orange;
    border: 1px solid $primary-blue;
    .plus-out {
      background-color: $primary-blue;
    }
  }
}
.plus-out {
  background-color: $primary-orange;
  display: inline-flex;
  margin-top: -1px;
  height: 40px;
  width: 40px;
  float: right;
}
span.plus {
  background: url('../assets/svg/plus.svg') no-repeat right;
  background-size: contain;
  cursor: pointer;
  display: inline-block;
  height: 16px;
  width: 16px;
  margin: auto;
}
</style>
