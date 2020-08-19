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
  </div>
</template>

<script>
  export default {
    name: "Hero",
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
    margin-bottom: 5rem;
  }

  .bottom {
    margin-top: 5rem;
  }
</style>
