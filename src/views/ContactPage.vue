<template>
  <div class="mainCOmp">
    <Navbar />
    <div class="wrappingCOntact">
      <h2 class="numbered-heading">04. What’s Next?</h2>
      <h2 class="title12">Get In Touch</h2>
      <p class="paramain3" style="text-align: center; margin-top: 0px">
        First of all I wanna thank you for spending your precious time to know
        more about me. Although I’m not currently looking for any new
        opportunities, my inbox is always open. Whether you have a question or
        just want to say hi, I’ll try my best to get back to you!
      </p>
      <a
        class="email-link"
        href="mailto:ijas.ar@pitsolutions.com"
        rel="noopener noreferrer"
        target="_blank"
        >Say Hello</a
      >
      <ul class="unorderdIcons">
        <li class="socialList">
          <a href="https://www.instagram.com/ijas_abubacker/">
            <i class="fa-brands fa-instagram colors"></i
          ></a>
        </li>
        <li>
          <a href="https://github.com/Ijas10">
            <i class="fa-brands fa-github colors"></i
          ></a>
        </li>
        <li>
          <a href="https://www.linkedin.com/in/ijas-abubacker/">
            <i class="fa-brands fa-linkedin-in colors"></i
          ></a>
        </li>
        <li>
          <a href="mailto:ijas.ar@pitsolutions.com">
            <i class="fa-regular fa-envelope colors"></i
          ></a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import Navbar from "../components/TheNavbar.vue";
</script>

<style>
.wrappingCOntact {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 20px;
  height: 90vh;
  position: relative;
}
.paramain3 {
  font-family: "mySecFont2";
  font-size: 18px;
  line-height: 23.4px;
  color: #8892b0;
  margin-top: 40px;
  font-weight: 400;
}
.unorderdIcons {
  padding-left: 0px;
  list-style-type: none;
  display: flex;
  justify-content: space-around;
  width: 70%;
  margin-top: 40px;
  position: absolute;
  bottom: 10%;
}

/* .colors {
  color: #ccd6f6;

  font-size: 20px;
} */
a {
  color: #ccd6f6;
  font-size: 20px;
}

a:hover,
a:focus {
  color: #64ffda;
}
.title12 {
  font-size: 40px;
  font-family: "mySecFont";
  color: #ccd6f6;
  font-weight: 600;
  display: flex;
  line-height: 40px;
  align-items: center;

  margin-top: 20px;
}
.email-link {
  background-color: transparent;
  border: 1px solid #64ffda;
  color: #64ffda;
  font-family: "myFirstFont";

  border-radius: 6px;
  padding: 1.25rem 1.75rem;
  font-size: var(--fz-sm);

  line-height: 1;
  text-decoration: none;
  cursor: pointer;
  transition: var(--transition);
  margin-top: 50px;
}
.numbered-heading {
  color: #64ffda;
  font-family: "myFirstFont";
  font-size: 16px;
  font-weight: 400;
  line-height: 17.6px;
}
@media screen and (min-width: 678px) {
  .unorderdIcons {
    width: 30%;
  }
  .title12 {
    font-size: 51px;
    margin-top: 30px;
    margin-bottom: 20px;
  }
  .paramain3 {
    width: 50%;
    font-size: 20px;
  }
  a {
    font-size: 25px;
  }
}
</style>
