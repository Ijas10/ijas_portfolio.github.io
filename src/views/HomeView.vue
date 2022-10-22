<script>
import IntroPic from "../components/IntroPicComponent.vue";
import TheNavbar from "../components/TheNavbar.vue";

export default {
  data() {
    return {
      shown: true,
      delayed: false,
    };
  },
  mounted() {
    setTimeout(() => (this.shown = !this.shown), 2000);
  },
  components: {
    IntroPic,
    TheNavbar,
  },
  watch: {
    shown() {
      // do something with newValue and oldValue.
      setTimeout(() => (this.delayed = !this.delayed), 800);
    },
  },
  methods: {
    changeUrl1() {
      this.$router.push("/projects");
    },
  },
};
</script>

<template>
  <div class="mainCOmponent">
    <Transition>
      <IntroPic v-if="shown" />
    </Transition>
    <Transition>
      <div class="RemainingPage" v-if="delayed">
        <TheNavbar />
        <div class="firstContainer">
          <h1 class="header1">
            <span class="spanElementInCont">Hi, my name is </span> <br />Ijas
            Abubacker.
          </h1>
          <h1 class="subHeader">I build things for the web.</h1>
          <p class="paraIntro">
            I’m a Front-end developer specializing in building (and occasionally
            designing) exceptional digital experiences. Currently, I’m focused
            on building accessible, human-centered products at
            <a class="anchor" href="https://www.pitsolutions.ch/en/"
              >Pit Solutions</a
            >.
          </p>
          <button class="checkoutBtn" @click="changeUrl1">
            Check out my projects!
          </button>
        </div>
      </div>
    </Transition>
  </div>
</template>

<style scoped>
@import url(https://fonts.googleapis.com/css?family=Space+Mono);
@font-face {
  font-family: myFirstFont;
  src: url("../assets/SFMono-Regular-8799e6387338d58f2f137df821c86eb4.woff2");
}
@font-face {
  font-family: mySecFont;
  src: url("../assets/Calibre-Semibold-94fc73852539d6733dc0d80252c5e3fb.ttf");
}
@font-face {
  font-family: mySecFont2;
  src: url("../assets/Calibre-Regular-b0d4cbb1201155ddccc21d1b8059a670.woff2");
}

.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
.mainCOmponent {
  background-color: #0a192f;
  min-height: 100vh;
}
.logo {
  height: 40px;
  width: 150px;
}
.anchor {
  color: #64ffda;
  text-decoration: none;
}
.checkoutBtn {
  margin-top: 55px;
  background-color: transparent;
  border: 1px solid #64ffda;
  border-radius: 5px;
  color: #64ffda;
  font-size: 14px;
  width: 240px;
  height: 58px;
  font-family: "myFirstFont";
  cursor: pointer;
}
.paraIntro {
  color: #8892b0;
  font-size: 18px;
  line-height: 23.4px;
  font-family: "mySecFont2";
  margin-top: 15px;
}
.spanElementInCont {
  color: #64ffda;
  font-family: "myFirstFont";
  font-size: 17px;
  font-weight: 400;
}
.subHeader {
  font-family: "mysecFont";
  color: #8892b0;
  font-size: 40px;
  font-weight: 600;
  line-height: 36px;
  margin-top: 10px;
}
.navbar {
  display: flex;
  justify-content: space-between;
}
.header1 {
  color: #ccd6f6;
  font-size: 40px;
  font-weight: 600;
  font-family: "mySecFont";
  line-height: 46px;
}
.firstContainer {
  /* height: 90vh; */
  margin: 20px;
  margin-top: 80px;
  margin-left: 25px;
}
@media screen and (min-width: 678px) {
  .header1 {
    font-size: 80px;
    line-height: 88px;
  }
  .RemainingPage {
    display: flex;
    flex-direction: column;
  }
  .firstContainer {
    width: 80%;
    align-self: center;
  }
  .subHeader {
    font-size: 78px;
    line-height: 88px;
  }
  .paraIntro {
    font-size: 20px;
    width: 55%;
  }
}
@media screen and (min-height: 900px) {
  .firstContainer {
    margin-top: 160px;
  }
}
</style>
