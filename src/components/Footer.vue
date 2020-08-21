<template>
  <footer class="footer">
    <p>Copyright {{ date }} | Javad sharifzadeh-Najafi</p>
    <div id="social-media">
      <a
        v-for="link in footerLinks"
        :key="link.id"
        :href="link.href"
        target="_blank"
        ><img :src="'./images/footer/' + link.img" :alt="link.label" />
        <p>{{ link.label }}</p>
      </a>
    </div>
  </footer>
</template>

<script>
  export default {
    name: 'Footer',
    data() {
      return {
        date: '',
        footerLinks: [
          {
            label: 'Github',
            href: 'https://github.com/Jsharifz',
            img: 'github-square-brands.svg',
          },
          {
            label: 'LinkedIn',
            href: 'https://www.linkedin.com/in/javad-sharifzadeh-najafi/',
            img: 'linkedin-brands.svg',
          },
          {
            label: 'E-Mail',
            href: 'mailto:jsharifz@outlook.com',
            img: 'envelope-solid.svg',
          },
        ],
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
    display: flex;
    flex-direction: column;

    background-color: rgba(236, 255, 255, 0.9);
    padding: 10px 0 30px 0;
  }

  .footer p {
    padding-bottom: 1rem;
  }

  #social-media {
    display: flex;

    justify-content: center;
  }

  #social-media p {
    line-height: 0;
  }

  img {
    height: 50px;
    margin: 0 2rem;
  }
</style>
