<template>
  <li class="individualProjects">
    <h2 class="projectheader">
      {{ details.name }}
    </h2>
    <div :class="details.classname"  >
      <div class="wrapped">
        <p class="paramain">
          {{ details.description }}
        </p>
        <ul class="skills-list">
          <li class="listEl" v-for="each in details.techs" :key="each">
            {{ each }}
          </li>
        </ul>
      </div>
      <img :src="details.imgurl" class="projectImage" alt="img" />
    </div>
    <a :href="details.link" @click="showpopup" class="linkOf1">Demo</a>
  </li>
</template>

<script>
export default {
  props: ["details"],
  methods: {
    showpopup() {
      if (this.details.id <= 2) {
        alert(
          "Please note that you must login with the given credentials to view the project. \n  {{ \n Username: raja , \n password: raja@2021 \n }}"
        );
      }
    },
  },
};
</script>

<style>
.linkOf1 {
  position: absolute;
  font-size: 20px;
  right: 25px;
  bottom: 25px;
  color: #64ffda;
  font-family: "myFirstFont";
}
.projectImage {
  width: 100%;
  display: none;
  /* display: none; */
}
@media screen and (min-width: 678px) {
  .projectImage {
    display: block;
    border-radius: 8px;
    width: 50%;
    height: 50%;
    
    
  }
  .divClass {
    display: flex;
    align-items: center;
  }
  .wrapped {
    width: 50%;
    margin-left: 30px;
  }
  .extraclass{
    display:flex;
    flex-direction: row-reverse;
    
  }
  
  
}
@media screen and ( min-width:1751px){
  .projectImage {
    margin-top:40px;
  }
}
</style>
