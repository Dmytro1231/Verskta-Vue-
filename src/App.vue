<template>
  <Header />
  <Hero />
  <Form />
  <TextBlock />
  <Footer />
</template>

<script>
import Header from "@/components/Header";
import Hero from "@/components/Hero";
import Form from "@/components/Form";
import TextBlock from "@/components/TextBlock";
import Footer from "@/components/Footer";

export default {
  name: "App",
  components: {
    Header,
    Hero,
    Form,
    TextBlock,
    Footer,
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Rubik:wght@300;400;700&display=swap");

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
html,
body {
  font-family: Roboto, Helvetica, Arial, sans-serif;
}
.btn {
  display: block;
  outline: none;
  cursor: pointer;
  border: none;
  background: #e96b2c;
  border-radius: 5px;
  padding: 16px 47px 13px 47px;
  margin-top: 40px;
  font-weight: bold;
  font-size: 20px;
  line-height: 24px;
  color: #fff;
  text-align: center;
}
.btn:hover,
.btn:focus {
  transition: background 0.3s ease-out;
  background: #ff994f;
  box-shadow: 0px 0px 20px rgba(255, 163, 79, 0.5);
}

.btn:focus {
  outline: 1px solid #fff;
  outline-offset: -4px;
}
</style>
