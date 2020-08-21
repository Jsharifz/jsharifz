<template>
  <div class="stacks">
    <div
      v-for="stack in stackList"
      id="stack-card"
      :key="stack.id"
      :class="stack.class"
    >
      <img :alt="stack.name" :src="'./vforimages/stack/' + stack.svg" />
      <p>{{ stack.name }}</p>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Stacks',
    data() {
      return {
        stackList: [
          {
            name: 'HTML5',
            class: 'icon-alt-1',
            svg: 'html5-brands.svg',
          },
          {
            name: 'CSS3',
            class: 'icon-alt-2',
            svg: 'css3-alt-brands.svg',
          },
          {
            name: 'Sass',
            class: 'icon-alt-1',
            svg: 'sass-brands.svg',
          },
          {
            name: 'JavaScript',
            class: 'icon-alt-2',
            svg: 'js-square-brands.svg',
          },
          {
            name: 'Node Package Manager',
            class: 'icon-alt-1',
            svg: 'npm-brands.svg',
          },
          {
            name: 'Node.js',
            class: 'icon-alt-2',
            svg: 'node-js-brands.svg',
          },
          {
            name: 'Vue.js',
            class: 'icon-alt-1',
            svg: 'Vue.js_Logo_2.svg',
          },
          {
            name: 'Adobe Suite',
            class: 'icon-alt-2',
            svg: 'adobe-brands.svg',
          },
          {
            name: 'Jekyll',
            class: 'icon-alt-1',
            svg: 'jekyll.svg',
          },
          {
            name: 'WordPress',
            class: 'icon-alt-2',
            svg: 'wordpress-brands.svg',
          },
          {
            name: 'Shopify',
            class: 'icon-alt-1',
            svg: 'shopify_glyph.svg',
          },
        ],
      };
    },
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .stacks {
    display: flex;
    flex-wrap: wrap;
    margin-top: 1rem;
    width: 100%;
    justify-content: center;
  }

  #stack-card {
    display: flex;
    flex-direction: column;
    width: 100px;
    justify-content: center;
    align-items: center;
    height: 175px;
    padding: 0.75rem 1rem;
    margin: 0.75rem;
    border-radius: 15px;
    background-image: radial-gradient(
      rgba(236, 255, 255, 0),
      rgba(236, 255, 255, 0.9)
    );
  }

  #stack-card img {
    width: 100px;
  }

  .icon-alt-1 {
    animation: sprite1 5s infinite ease-in-out;
  }

  @keyframes sprite1 {
    0% {
      transform: translateY(10px);
    }
    50% {
      transform: translateY(-10px);
    }
    100% {
      transform: translateY(10px);
    }
  }

  .icon-alt-2 {
    animation: sprite2 5s infinite ease-in-out;
  }

  @keyframes sprite2 {
    0% {
      transform: translateY(-10px);
    }
    50% {
      transform: translateY(10px);
    }
    100% {
      transform: translateY(-10px);
    }
  }
</style>
