<template>
  <div class="main-text">
    <div class="section-heading">
      <p>Section Heading</p>
    </div>
    <div class="title-text">
      <p>
        Highlight paragraph duis aute irure dolor in reprehenderit
        in voluptate velit energy efficiency eu di fugiat.
      </p>
    </div>
    <div class="paragraph-text">
      <p>Sed ut perspiciatis unde omnis iste natus
        error sit voluptatem accusantium doloremque laudantium, totam rem aperiam,
        eaque ipsa quae ab illo inventore veritatis et quasi ventus vitae ventus
        consecutem terra lora magnum lorem aqua.
      </p>
    </div>
    <Button text="BUTTON" class="button"/>
  </div>
</template>

<script>
import Button from './Button.vue';

export default {
  name: 'main-text',
  components: {
    Button,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_variables.scss";

.main-text {
  padding-top: 30px;
  @media screen and (max-width: 2920px) {
    padding-top: 80px;
  }
  @media screen and (max-width: 1366px) {
    padding-top: 60px;
  }
  @media screen and (max-width: 768px) {
    padding-top: 50px;
  }
  @media screen and (max-width: 375px) {
    padding-top: 30px;
  }
  @media screen and (min-width: 768px) {
    display: inline-block;
  }
}

.section-heading {
  color: #BEBEBE;
  font-family: $secondary-font-family;
  font-size: 14px;
  font-weight: bold;
  letter-spacing: 1.2px;
  line-height: 24px;
  text-transform: uppercase;
  @media screen and (max-width: 1366px) {
    font-size: 18px;
    line-height: 28px;
  }
}
.title-text {
  color: $primary-blue;
  font-size: 22px;
  font-weight: 900;
  line-height: 34px;
  margin-top: 10px;
  @media screen and (min-width: 1366px) {
    margin-top: 20px;
    font-size: 30px;
    line-height: 44px;
  }
  @media screen and (min-width: 768px) {
    font-size: 24px;
    line-height: 38px;
  }
}
.paragraph-text {
  color: #191919;
  font-size: 14px;
  font-weight: 600;
  line-height: 28px;
  margin-top: 20px;
  @media screen and (min-width: 1366px) {
    margin-top: 30px;
    font-size: 16px;
    line-height: 30px;
    width: 500px;
  }
}
.button {
  margin-top: 20px;
  @media screen and (min-width: 768px) {
    margin-bottom: 10px;
  }
}
</style>
