<template>
  <div class="mainCOmp">
    <TheNavbar />

    <div class="secondDiv">
      <h1 class="headerMain">About Me</h1>
      <div class="wrapperdiv">
        <div class="paraWrapper">
          <p class="paramain">
            Hello! My name is
            <span style="color: #64ffda">Ijas Abubacker</span> and I enjoy creating things
            that live on the internet. I graduated in Bsc Botany And Biotechnology in the year 2020(yes I was a non IT graduate and you might be probably thinking how I ended up here ). During the pandemic session I came across some youtube videos regarding web development and designing. One video after another I gradually fell in love with this whole development process.
          </p>
          <p class="paramain" style="margin-top:20px">Then after a few months I decided to take this interest to the next level. I joined a Full-stack Web development course provided by <a style="color: #64ffda ; text-decoration : none ; font-size:18px" href="https://www.ccbp.in/intensive?gclid=Cj0KCQjwhsmaBhCvARIsAIbEbH4SAwDLRp1zR2BCYgnG8G3T_5f__539i2UTEzJwI2aq4W-iBsJpmWUaAn_8EALw_wcB" class="">Nxtwave 4.0 Technologies</a></p>
          <p class="paramain" style="margin-top:20px"> I gained so much knowledge about both front-end and back-end technologies but I easily figured it out that front-end was my cup of tea. Now I'm woking as Associate Front-end Developer in <a href="https://www.pitsolutions.ch/en/" style="color: #64ffda ; text-decoration : none ; font-size:18px">Pit Solutions</a>
            Here are a few technologies I’ve been working with recently:
          </p>

          <ul class="skills-list">
            <li class="listEl">JavaScript (ES6+)</li>
            <li class="listEl">Vue.JS</li>
            <li class="listEl">React</li>
            <li class="listEl">Express.JS</li>
            <li class="listEl">Node.JS</li>
            <li class="listEl">Sqlite</li>
            <li class="listEl">Python</li>
          </ul>
        </div>

        <div class="divWrapper">
          <img
            src="https://res.cloudinary.com/dnlxvy81c/image/upload/v1665051909/WhatsApp_Image_2022-09-30_at_3.15.47_PM_ky1kqm.jpg"
            alt="ijas abubacker pic"
            class="imgOfMine"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TheNavbar from "../components/TheNavbar.vue";
export default {
  components: {
    TheNavbar,
  },
};
</script>

<style>
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
.spanElment {
  color: #64ffda;
  font-family: "Space Mono";
  font-size: 17px;
}
.paramain {
  font-family: "mySecFont2";
  font-size: 18px;
  line-height: 23.4px;
  color: #8892b0;
  margin-top: 40px;
  font-weight: 400;
}
/* .divWrapper {
  display: flex;
  justify-content: center;
} */
.listEl {
  width: 50%;
  position: relative;
  display: flex;
  align-items: center;
  margin-bottom: 8px;

  padding-left: 20px;
  font-size: 13px;
  font-family: "myFirstFont";
}
.listEl::before {
  content: "▹";
  position: absolute;
  left: 0px;
  color: #64ffda;
  font-size: 14px;
  line-height: 12px;
}
.hori {
  display: flex;
  transform: rotate(90deg);
}
.secondDiv {
  padding: 20px;
}
.imgOfMine {
  width: 70%;
}

.divWrapper {
  /* width: 979px;
  height: 374px; */
  border-radius: 20px;

  overflow: hidden;
  margin-top: 40px;
}

.divWrapper img {
  width: 450px;
  height: 500px;
  margin: -105px 0 -53px -75px;
  border-radius: 20px;
}

.skills-list {
  list-style-type: none;
  padding-left: 0px;
  display: flex;
  flex-wrap: wrap;
  font-family: "mySecFont2";
  font-size: 18px;
  line-height: 23.4px;
  color: #8892b0;
  margin-top: 25px;
  margin-bottom: 40px;
}
.headerMain {
  font-size: 30px;
  font-family: "mySecFont";
  color: #ccd6f6;
  font-weight: 600;
  display: flex;
  align-items: center;
}
.headerMain::before {
  position: relative;
  bottom: 2px;
  counter-increment: section 1;
  content: "0" counter(section) ".";
  margin-right: 5px;
  color: #64ffda;
  font-family: "Space Mono";
  font-size: 17px;
  font-weight: 400;
}
.headerMain::after {
  content: "";
  display: flex;
  position: relative;
  top: -5px;
  width: 50%;
  height: 1px;
  margin-left: 8px;
  background-color: #233554;
}
.mainCOmp {
  background-color: #0a192f;
  min-height: 100vh;
}
@media screen and (min-width: 678px) {
  .secondDiv {
    width: 80%;
    align-self: center;
    justify-content: center;
    margin-top: 50px;
  }
  .headerMain::after {
    width: calc(60% - 22%);

    margin-left: 10px;
  }
  .paramain {
    font-size: 20px;
    line-height: 26.4px;
  }
  .headerMain {
    font-size: 32px;
    line-height: 35px;
  }
  .mainCOmp {
    display: flex;

    flex-direction: column;
  }
  .wrapperdiv {
    display: flex;
  }
  .imgOfMine {
    width: 400px;
    height: 400px;
  }
  .paraWrapper {
    width: 60%;
  }
  .paramain {
    width: 90%;
  }
  .divWrapper {
    border-radius: 0px;
  }
  .divWrapper img {
    border-radius: 0px;
  }
}
</style>
