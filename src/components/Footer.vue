<template>
  <footer class="footer">
    <p>Copyright {{ date }} | Javad sharifzadeh-Najafi</p>
    <a href="https://github.com/Jsharifz" target="_blank"
      ><img src=".././assets/footer/github-square-brands.svg" alt=""
    /></a>
    <a
      href="https://www.linkedin.com/in/javad-sharifzadeh-najafi/"
      target="_blank"
      ><img src=".././assets/footer/linkedin-brands.svg" alt="" />
    </a>
    <a href="mailto:jsharifz@outlook.com"
      ><img src=".././assets/footer/envelope-solid.svg" alt=""
    /></a>
  </footer>
</template>

<script>
  export default {
    name: "Footer",
    data() {
      return {
        date: "",
      };
    },
    created() {
      this.date = new Date().getFullYear();
    },
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .footer {
    background-color: rgba(236, 255, 255, 0.9);
    padding: 10px 0 30px 0;
  }

  .footer p {
    padding-bottom: 1rem;
  }

  img {
    height: 75px;
    margin: 0 10px;
  }
</style>
