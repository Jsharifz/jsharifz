<template>
  <div class="projects">
    <div id="project-card" v-for="project in projectList" :key="project.id">
      <a :href="project.deployment" target="blank">
        <h3>{{ project.title }}</h3>
      </a>
      <p>{{ project.descrption }}</p>
      <a :href="project.repo" target="blank">
        <h3>Repository</h3>
      </a>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Projects",
    data() {
      return {
        projectList: [
          {
            title: `JavaScript API App`,
            descrption: "Description",
            deployment:
              "https://jsharifz.github.io/JavaScript-Assignments/js-assignment3/index.html",
            repo: `https://github.com/Jsharifz/JavaScript-Assignments/tree/master/js-assignment3`,
          },
          {
            title: `Sass Wireframe Project`,
            descrption: "Description",
            deployment:
              "https://jsharifz.github.io/projects/project%203/home.html",
            repo: `https://github.com/Vaddeil/sass-group-assignment`,
          },
          {
            title: `WordPress Website Redesign: APCSE`,
            descrption: "Description",
            deployment: "https://apcse.com/",
            repo: `https://apcse.com/`,
          },
          {
            title: `Express EJS3 Gallery`,
            descrption: "Description",
            deployment: "https://javad-node-assignment-3.herokuapp.com/",
            repo: `https://github.com/Jsharifz/Node-Assignment-3`,
          },
          {
            title: `Vue.js Website Redesign: Homa Health Care Services`,
            descrption: "Description",
            deployment:
              "http://https://homa-health-care-services.herokuapp.com",
            repo: `https://github.com/Jsharifz/homa-health-care-services`,
          },
          {
            title: `CSS Digital Watch`,
            descrption: "Description",
            deployment: "https://jsharifz.github.io/Bulova-Watch/",
            repo: `https://github.com/Jsharifz/Bulova-Watch`,
          },
          {
            title: `JavaScript Mini App`,
            descrption: "Description",
            deployment: "https://jsharifz.github.io/Pi-Estimator/",
            repo: `https://github.com/Jsharifz/Pi-Estimator`,
          },
          {
            title: `Vue.js Mini App`,
            descrption: "Description",
            deployment: "https://jsharifz.github.io/Pi-Estimator-Vue/",
            repo: `https://github.com/Jsharifz/Pi-Estimator-Vue`,
          },
        ],
      };
    },
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .projects {
    display: flex;
    flex-wrap: wrap;

    margin-top: 1rem;

    width: 100%;

    justify-content: center;
  }

  #project-card {
    width: 450px;
    min-width: 300px;

    padding: 1.5rem;
    margin: 1rem;
    border-radius: 15px;

    background-color: rgba(236, 255, 255, 0.9);
  }
</style>
