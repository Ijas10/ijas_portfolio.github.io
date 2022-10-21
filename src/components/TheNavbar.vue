<template>
  <div class="NavbarMain">
    <router-link to="/">
      <img
        src="https://res.cloudinary.com/dnlxvy81c/image/upload/v1665576805/Ijas_vcmpkg.jpg"
        alt="ijas.jpg"
        class="myPic"
      />
    </router-link>

    <div
      @click="hamburgerOpen = !hamburgerOpen"
      class="hamburger-icon"
      id="icon"
    >
      <div :class="!hamburgerOpen ? 'icon-1' : 'icon-1 icon-1a'" id="a"></div>
      <div :class="!hamburgerOpen ? 'icon-2' : 'icon-2c icon-1'" id="a"></div>
      <div :class="!hamburgerOpen ? 'icon-3' : 'icon-3b icon-3'" id="a"></div>
      <div class="clear"></div>
    </div>

    <nav id="nav" :class="!hamburgerOpen ? 'nav' : 'show'">
      <ul class="colored" v-if="hamburgerOpen">
        <li>
          <span class="spanElment">01.</span>
          <router-link class="routerlink" to="/about">About</router-link>
        </li>
        <!-- <li>
          <span class="spanElment">02.</span
          ><router-link class="routerlink" to="/experience"
            >Experience</router-link
          >
        </li> -->
        <li>
          <span class="spanElment">02.</span
          ><router-link class="routerlink" to="/projects">Work</router-link>
        </li>
        <li>
          <span class="spanElment">03.</span
          ><router-link class="routerlink" to="/contact">Contact</router-link>
        </li>
        <li class="flexBtn">
          <button  @click="urlOpen" class="resumeButoon">Resume</button>
        </li>
      </ul>
    </nav>

    <ul class="unorderlistInHeader">
      <li>
        <span class="spanElment">01.</span>
        <router-link class="routerlink" to="/about">About</router-link>
      </li>
      <!-- <li>
        <span class="spanElment">02.</span
        ><router-link class="routerlink" to="/experience"
          >Experience</router-link
        >
      </li> -->
      <li>
        <span class="spanElment">02.</span
        ><router-link class="routerlink" to="/projects">Work</router-link>
      </li>
      <li>
        <span class="spanElment">03.</span
        ><router-link class="routerlink" to="/contact">Contact</router-link>
      </li>
      <li>
        <!-- <a href="https://tinyurl.com/ydwxe7cr" class="resumeButoon">Resume</a> -->
        <button class="resumeButoon" @click="urlOpen">Resume</button>
      
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  data() {
    return {
      hamburgerOpen: false,
      burgerStyle: {
        "--padding": "10px",
        "--layer-bg-color": "yellow",
        "--active-layer-bg-color": "#ABABAB",
        "--layer-width": "20px",
      },
    };
  },
  methods : {
    urlOpen() {
      window.open('https://tinyurl.com/ydwxe7cr')
    }
  }
  
};
</script>

<style scoped>
@import url(https://fonts.googleapis.com/css?family=Montserrat:400,700);
@import url(https://fonts.googleapis.com/css?family=Orbitron);
@import url(https://fonts.googleapis.com/css?family=Space+Mono);
@font-face {
  font-family: myFirstFont;
  src: url("../assets/SFMono-Regular-8799e6387338d58f2f137df821c86eb4.woff2");
}
body {
  font-family: "montserrat", roboto;
}
.myPic {
  width: 130px;
  height: 30px;
  margin-left: 10px;
}
.routerlink {
  text-decoration: none;
  color: #ccd6f6;
  font-size: 15px;
  font-family: "myFirstFont";
}
.routerlink:hover {
  color: #64ffda;
}
.flexBtn {
  display: flex;
  justify-content: center;
  margin-top: 60px;
}
.NavbarMain {
  padding-top: 30px;
  padding-left: 10px;
  height: 10vh;
}
.unorderlistInHeader {
  display: flex;
  list-style-type: none;
  padding-left: 0px;
  display: none;
}
.adding {
  background-color: yellow;
  height: 30px;
  width: 30px;
}
.colored {
  padding-left: 0px;
}

header {
  width: 100%;
  height: 100%;

  position: absolute;
  overflow: auto;
}
.resumeButoon {
  margin-top: -5px;
  background-color: transparent;
  border: 1px solid #64ffda;
  border-radius: 5px;
  color: #64ffda;
  font-size: 16px;
  width: 170px;
  height: 38px;
  cursor: pointer;
}
.icon-1,
.icon-2,
.icon-3 {
  position: absolute;
  left: 26%;
  top: 50%;
  width: 25px;
  height: 2px;
  background-color: #64ffda;
  transition: all 400ms cubic-bezier(0.84, 0.06, 0.52, 1.8);
}

.icon-1 {
  transform: translateY(-8px);
  animation-delay: 100ms;
}

.icon-3 {
  transform: translateY(8px);
  animation-delay: 250ms;
}

.hamburger-icon {
  height: 50px;
  width: 50px;
  top: 24%;
  /* left: 3%; */
  right: 20px;
  position: absolute;
  z-index: 1000;
  cursor: pointer;
  border-radius: 50%;
  transition: all 0.2s ease-in-out;
  /* background: rgba(255, 255, 255, 0.2); */
}
.hamburger-icon:hover {
  transform: scale(1.2);

  box-shadow: 0px 0px 30px rgba(0, 0, 0, 0.1);
}

.icon-1a {
  transform: rotate(40deg);
}

.icon-3b {
  transform: rotate(-40deg);
}

.icon-2c {
  opacity: 0;
}

.clear {
  clear: both;
}

/* @keyframes slideIn {
  0% {
    width: 0%;
    opacity: 0;
  }
  100% {
    width: 50%;
    opacity: 1;
  }
} */
nav {
  background: #112240;
  position: absolute;
  top: 0;
  right: 0;
  height: 100vh;
  width: 0%;
  z-index: 10;
  opacity: 0;
  transition: all 600ms cubic-bezier(0.62, 0.04, 0.3, 1.56);
  transition-delay: 100ms;
  display: flex;
  justify-content: center;
  align-items: center;
}
nav ul {
  margin: 0;
  position: absolute;
  /* top: 30%;
  right: 50; */
}
nav ul li {
  list-style: none;
  font-size: 24px;
  color: #fff;
  line-height: 2;

  letter-spacing: 1.7px;
}
.show {
  width: 60%;
  opacity: 1;
}
.spanElment {
  color: #64ffda;
  font-family: "Space Mono";
  font-size: 14px;
}

.dark-blue {
  position: absolute;
  top: 0;
  left: 0;
  background: #64b5f6;
  height: 100%;
  width: 0%;
  transition: all 500ms cubic-bezier(0.62, 0.04, 0.3, 1.8);
  transition-delay: 50ms;
  z-index: 5;
  opacity: 1;
}

.slide {
  width: 50%;
  opacity: 1;
}
/*
@keyframes shotup {
  0% {
    transform: translate(300%);
    opacity: 0;
  }
  90% {
    transform: translateY(-50px);
  }
  100% {
    transform: translateY(0%);
    opacity: 1;
  }
} */
@media screen and (min-width: 678px) {
  .hamburger-icon,
  .colored {
    display: none;
  }
  .resumeButoon {
    width: 100px;
  }
  .myPic {
    width: 190px;
    height: 38px;
    margin-left: 30px;
  }
  .unorderlistInHeader {
    display: flex;
    width: 450px;
    color: #ccd6f6;
    justify-content: space-between;
    top: 49%;
    /* left: 3%; */
    right: 40px;
    font-size: 17px;

    position: absolute;
  }
}
</style>
