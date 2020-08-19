<template>
  <div class="hero">
    <div class="top">
      <h1>Javad Sharifzadeh-Najafi</h1>
      <h2>Web Developer & Designer</h2>
    </div>

    <div class="bottom">
      <h1>Customizing Experience</h1>
      <h2>Since 2020</h2>
    </div>
    <a
      class="resume-button"
      href="Javad Sharifzadeh-Najafi - Resume.pdf"
      target="blank"
      >Resume</a
    >
  </div>
</template>

<script>
  export default {
    name: 'Hero',
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .hero {
    display: flex;
    flex-direction: column;

    justify-content: center;

    height: 800px;

    background-image: linear-gradient(
      rgba(236, 255, 255, 0.9) 90%,
      rgba(236, 255, 255, 0)
    );
  }

  .hero h1 {
    font-size: 3rem;
  }

  .top {
    margin-bottom: 3rem;
  }

  .bottom {
    margin-top: 3rem;
  }

  .resume-button {
    display: flex;

    font-size: 1.5rem;

    padding: 1rem 2rem;
    border-radius: 1rem;

    width: max-content;
    margin: 2rem auto;

    border-bottom: solid 7px rgba(0, 0, 0, 0);
    background-color: rgb(206, 241, 255);

    transition: ease-out 0.25s;
  }

  .resume-button:hover {
    transform: rotateX(30deg);
    border-bottom: solid 7px skyblue;
    background-color: rgb(232, 248, 255);
  }
</style>
