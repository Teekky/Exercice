<template>
  <h1>HelloWorld</h1>
  <ul id="hide" v-if="seen">
    <li v-for="item in items" :key="item.message">
      {{ item.message }}
    </li>
  </ul>

  <div id="app" v-on:click="seen = !seen" class="control">
    <a id="button">Hide WATA</a>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      items: [
        { message: "One Day" },
        { message: "Two Days" },
        { message: "Three Days" },
        { message: "Four Days" },
        { message: "Five Days" },
      ],
      isHidden: false,
      seen: true,
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
  color: white;
}

#button {
  background-color: #42b983;
  padding: 1em;
  cursor: pointer;
}

</style>
