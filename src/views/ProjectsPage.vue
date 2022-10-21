<template>
  <div class="mainCOmp">
    <Navbar />
    <div class="secondDiv">
      <h1 class="headerMain2">Some Things I've Built</h1>
      <ul class="projectsHolder">
        <IndividualDetails
          v-for="each in listof"
          :details="each"
          :key="each.id"
        />
      </ul>
    </div>
  </div>
</template>

<script setup>
import IndividualDetails from "../components/IndividualDetails.vue";
import Navbar from "../components/TheNavbar.vue";
const listof = [
  {
    name: "Nxt Trendz (ECommerce Clone)",
    id: 1,
    link: "https://ijasnxttrndsapp.ccbp.tech/",
    imgurl:
      "https://res.cloudinary.com/dnlxvy81c/image/upload/v1666249286/Screenshot_95_ujv1nc.png",

    techs: ["React.JS", "HTML", "CSS", "Bootstrap", "Docker"],
    classname : 'divClass extraclass',
    description:
      "Implemented Nxt Trendz application which is a clone for ECommerce applications like Amazon, Flipkart where users can login and can see list of products. Developed different pages and routes for Login, Products, Product details using React Router components like Route, Switch, Link and Props. Persisted user login state by keeping jwt token in local storage and also sending it in headers of further api calls to authorize the user. ",
  },
  {
    name: "Book Hub (Goodreads Clone)",
    id: 2,
    link: "https://ijasbookhubapp.ccbp.tech/",
    imgurl:
      "https://res.cloudinary.com/dnlxvy81c/image/upload/v1666250025/Screenshot_96_dmnswa.png",

    techs: ["React.JS", "React Select", "HTML", "CSS", "Bootstrap", "Docker"],
    classname:'divClass',

    description:
      "Implemented responsive Goodreads Clone where users can log in and see a list of books. All the books are sorted into different shelves based on different categories. Users can also search for a particular book. Implemented different routes for features like login, home, bookshelves by using React Router components. Used Figma mockups to implement UI-rich and pixel-perfect React components. Implemented username and password authentication and persisted login state using client storage.",
  },
  {
    name: "Movie DB",
    id: 3,
    link: "https://moviedb-initial.web.app/",
    imgurl:
      "https://res.cloudinary.com/dnlxvy81c/image/upload/v1666250080/Screenshot_98_a7mlpj.png",
    techs: ["Vue.JS", "Firebase", "Vuex", "HTML", "CSS"],
    classname : 'divClass extraclass',
    description:
      "Build a website which displays all the latest and popular movies by retrieving data from movieDB API. Also achieved other functionalities like searching and sorting based on rating and alphabetical order. Users can login or even sign-up to the app and they can also add movies to the favourites page based on their likes. Implemented user authentication by using firebase which allows only auntheticated users to access all the pages",
  },
  {
    name: "Sharjah Police Meta",
    id: 4,
    link: "https://routingproject-9a37a.web.app/",
    imgurl:
      "https://res.cloudinary.com/dnlxvy81c/image/upload/v1666250141/Screenshot_99_yrkkm1.png",
    techs: [
      "Vue.JS",
      "Firebase",
      "CSS",
      "Vuex",
      "Speechly Polyfill",
      "Web Speech Api",
    ],
    classname:'divClass',
    description:
      "Developed a speech recognition application which is a crucial part of the meta concepts and integrated it to the Sharjah police website. The full application runs on speech recognition and speech synthesis. Users can fill the form by simply saying the words we used to type which was a very time consuming process .And after going through the login and selecting avatar pages users are directed to a Virtual Reality page where we can control our avatar and do lot of things ",
  },
];
</script>

<style>
.projectsHolder {
  list-style-type: none;
  padding-left: 0px;
}
.headerMain2 {
  font-size: 26px;
  font-family: "mySecFont";
  color: #ccd6f6;
  font-weight: 600;
  display: flex;
  align-items: center;
  margin-bottom: 30px;
}
.projectheader {
  font-size: 24px;
  font-weight: 600;
  line-height: 26px;
  color: #64ffda;
  font-family: "mySecFont";
  margin-top: 15px;
}
.individualProjects {
  padding: 20px;
  background: #233554;
  border-radius: 9px;
  margin-bottom: 20px;
  position: relative;
}

.headerMain2::before {
  position: relative;
  bottom: 2px;
  counter-increment: section 1;
  content: "03" ".";
  margin-right: 5px;
  color: #64ffda;
  font-family: "Space Mono";
  font-size: 17px;
  font-weight: 400;
}
.headerMain2::after {
  content: "";
  display: flex;
  position: relative;
  top: -5px;
  width: 20%;
  height: 1px;
  margin-left: 8px;
  background-color: #233554;
}
.projectsFirstCOnt {
  padding: 20px;
}
@media screen and (min-width: 678px) {
  .headerMain2 {
    font-size: 32px;
    line-height: 35px;
  }
  .headerMain2::after {
    width: calc(60% - 22%);

    margin-left: 19px;
  }
  
}
</style>
