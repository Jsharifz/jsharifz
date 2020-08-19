<template>
  <div class="contact">
    <form action="https://formspree.io/xyypdjlq" method="POST">
      <label for="name">Name</label>
      <input type="text" name="name" id="name" required />
      <label for="email">E-Mail</label>
      <input type="email" name="_replyto" id="email" required />
      <label for="subject">Subject</label>
      <input type="text" name="subject" id="subject" required />
      <label for="message">Message</label>
      <textarea
        name="message"
        id="message"
        cols="30"
        rows="10"
        placeholder="Insert your message here"
        required
      ></textarea>
      <input type="submit" id="submit" value="Send Message" />
    </form>
  </div>
</template>

<script>
  export default {
    name: "Contact",
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .contact {
    display: block;

    text-align: left;

    padding: 3rem 0;

    width: 100%;
    background-image: linear-gradient(
      rgba(236, 255, 255, 0),
      rgba(236, 255, 255, 0.9) 5%
    );
  }

  form {
    display: flex;
    flex-direction: column;

    padding: 1rem 1.5rem;
    border-radius: 1rem;

    margin: auto;

    max-width: 750px;
  }

  form * {
    border-radius: 0.5rem;
  }

  #name,
  #email,
  #submit,
  #subject {
    padding: 0.5rem;
  }

  #submit {
    margin: 0.5rem 0;
    transition: 0.25s;
  }

  #submit:hover {
    background: rgb(214, 214, 255);
  }

  label {
    padding-top: 0.5rem;
  }

  input,
  textarea {
    padding: 0.5rem;
    border: 1px solid rgb(185, 185, 185);
  }
</style>
