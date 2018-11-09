<template>
  <div class="listt columns">
    <div class="column is-3-tablet">
      <span class="x">01</span>
      <span class="icon"></span>
      <p>Icon Label Lorem Ipsum Terra</p>
    </div>
    <div class="column is-3-tablet">
      <span class="x">02</span>
      <span class="icon"></span>
      <p>Icon Label Lorem</p>
    </div>
    <div class="column is-3-tablet">
      <span class="x">03</span>
      <span class="icon"></span>
      <p>Icon Label Lorem Ipsum</p>
    </div>
    <div class="column is-3-tablet">
      <span class="x">04</span>
      <span class="icon"></span>
      <p>Icon Label</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'List',
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_variables.scss";

.listt {
  position: relative;
  margin: 20px 10px;
  @media screen and (min-width: 768px) {
    margin: 100px 24px 30px;
  }
  margin-left: 0;
  color: $primary-blue;
  font-family: $secondary-font-family;
  font-size: 12px;
  font-weight: bold;
  letter-spacing: 1.4px;
  text-transform: uppercase;
  line-height: 20px;
  div {
    padding-top: 10px;
    display: flex;
    align-items: center;
  }
  max-width: 701px;
  @media screen and (max-width: 1366px) {
    max-width: 500px;
  }
  @media screen and (max-width: 768px) {
    max-width: 344px;
  }
  @media screen and (max-width: 375px) {
    max-width: 335px;
  }
}
span.icon {
  background: url('../assets/svg/icon.svg') no-repeat right;
  background-size: contain;
  cursor: pointer;
  display: inline-block;
  height: 50px;
  width: 50px;
  @media screen and (max-width: 2920px) {
    height: 80px;
    width: 80px;
  }
  @media screen and (max-width: 1366px) {
    height: 70px;
    width: 70px;
  }
  @media screen and (min-width: 769px) {
    margin: 0 auto;
  }
  @media screen and (max-width: 768px) {
    height: 39px;
    width: 39px;
  }
  @media screen and (max-width: 375px) {
    height: 37px;
    width: 37px;
  }
  margin-right: 21px;
}
.column {
  @media screen and (min-width: 769px) {
    display: block !important;
    text-align: center;
    position: relative;
    width: 110px;
    p {
      width: 120px;
      margin: 0 auto;
    }
  }
  &:not(last-child) {
    margin-bottom: 18px;
  }
}
.x {
  font-family: $primary-font-family;
  font-weight: 900;
  color: #E5E5E5;
  font-size: 36px;
  line-height: 46px;
  position: absolute;
  margin-top: -50px;
  margin-left: -22px;
  @media screen and (max-width: 2920px) {
    margin-top: -80px;
  }
  @media screen and (max-width: 1366px) {
    margin-top: -50px;
    font-size: 36px;
    font-weight: 900;
  }
  @media screen and (min-width: 769px) {
    margin-top: -50px;
    font-size: 36px;
  }
  @media screen and (max-width: 768px) {
    height: 39px;
    width: 39px;
    display: none;
  }
  @media screen and (max-width: 375px) {
    height: 50px;
    width: 50px;
  }
}
</style>
