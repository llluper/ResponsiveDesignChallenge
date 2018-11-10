<template>
  <div id="app">
    <div class="top-section">
      <div class="columns xx">
        <div class="column is-6-tablet">
          <MainText />
          <List v-if="windowWidth < 768" class="list-home" />
          <img src="./assets/images/image-leaves.jpeg" alt="Leaves" class="square">
          <div class="last-button" v-if="windowWidth > 767">
            <Button text="BUTTON" class="button-home" />
          </div>
        </div>
        <div class="column is-6-tablet">
          <List v-if="windowWidth > 767" class="list-home" />
          <div>
            <img src="./assets/images/image-foxgates.jpeg" alt="Foxgates">
            <img src="./assets/images/image-ocean.jpeg" alt="Ocean">
          </div>
        </div>
        <Button v-if="windowWidth < 767" text="BUTTON" class="button-home second-button" />
      </div>
    </div>
  </div>
</template>

<script>
import Button from './components/Button.vue';
import List from './components/List.vue';
import MainText from '@/components/MainText.vue';

export default {
  name: 'app',
  components: {
    Button,
    List,
    MainText,
  },
  data() {
    return {
      isMobile: false,
      windowWidth: 0,
      windowHeight: 0,
    };
  },
  created() {
    this.isMobile = this.getWindowWidth();
  },
  mounted() {
    this.$nextTick(() => {
      window.addEventListener('resize', this.getWindowWidth);
      window.addEventListener('resize', this.getWindowHeight);

      this.getWindowWidth();
      this.getWindowHeight();
    });
  },
  methods: {
    getWindowWidth() {
      this.windowWidth = document.documentElement.clientWidth;
    },
    getWindowHeight() {
      this.windowHeight = document.documentElement.clientHeight;
    },
    beforeDestroy() {
      window.removeEventListener('resize', this.getWindowWidth);
      window.removeEventListener('resize', this.getWindowHeight);
    },
  },
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Muli:400,600,900|Roboto+Slab:700');
@import "./assets/scss/_variables.scss";

#app {
  margin: 20px 0 20px;
  font-family: $primary-font-family;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #fff;
  background-color: #F6F6F6;
  padding: 0 20px;
  padding-bottom: 40px;
  overflow-y: hidden;
  @media screen and (min-width: 769px) {
    margin: 40px 0 0 40px;
    padding-bottom: 40px;
  }
  @media screen and (max-width: 2920px) {
    margin: 100px 0 100px 162px;
    padding: 0 80px 80px;
  }
  @media screen and (max-width: 1366px) {
    margin: 80px 0 80px 115px;
    padding: 0 58px 58px;
  }
  @media screen and (max-width: 768px) {
    margin: 30px 0;
    padding: 0 30px 30px;
  }
  @media screen and (max-width: 375px) {
    margin: 20px 0;
    padding: 0 30px 30px;
  }
}
body, p {
  margin: 0;
}
#app .column {
  padding: 0;
  @media screen and (min-width: 768px) {
    &.is-6-tablet {
      -webkit-box-flex: 0;
      -ms-flex: none;
      flex: none;
      width: 50%;
    }
  }
}
.columns.xx {
  @media screen and (min-width: 768px) {
    display: flex;
  }
}
#app img {
  max-height: 480px;
  max-width: 100% !important;
  background-color: #D8D8D8;
  margin: 10px;
  display: block;
  @media screen and (min-width: 1367px) and (max-width: 1920px) {
    max-height: 480px;
    max-width: 701px;
    &.square {
      max-height: 701px;
    }
  }
  @media screen and (min-width: 769) and (max-width: 1366px) {
    max-height: 360px;
    max-width: 500px;
    &.square {
      max-height: 500px;
    }
  }
  @media screen and (min-width: 767px) and (max-width: 768px) {
    max-height: 234px;
    margin: 10px 5px;
    margin-left: 0;
  }
  @media screen and (min-width: 769px) {
    margin: 20px;
    &.square {
      margin-left: 0;
    }
  }
  @media screen and (max-width: 767px) {
    max-height: auto !important;
    max-width: 100% !important;
    margin: 20px 0;
    margin-left: 0;
  }
}
.list-home {
  padding-top: 10px;
  @media screen and (min-width: 769px) {
    padding-top: 40px;
  }
}
img.square {
  margin-top: 33px;
}
.last-button {
  display: block;
  padding: 0;
  @media screen and (min-width: 769px) {
    padding: 40px 0 33px;
  }
  @media screen and (max-width: 767px) {
    padding: 0;
  }
  margin-top: 20px;
}
.top-section  {
  margin-top: 20px;
}
.second-button{
  @media screen and (max-width: 767px) {
    margin-top: 20px;
    margin-bottom: 40px;
  }
}
</style>
