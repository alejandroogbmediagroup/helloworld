<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h3>{{ description }}</h3>
    <p>
      Daniel Otero is a young player of soccer of Sel. Valle and Colombia
      Paralimpic.
      <a
        href="https://www.youtube.com/watch?v=g1T1JBZSkB0"
        target="_blank"
        rel="noopener"
        >Skills Daniel Otero</a
      >.
    </p>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      description:
        "His position is midfielder, he have very big talents is vision, assistants and goals.",
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
