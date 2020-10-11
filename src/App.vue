<template>
  <div id="app">
    <hr />
    <!-- Normal -->
    <input v-model="message" placeholder="edit me" />
    <p>Normal Message is: {{ message }}</p>
    <hr />

    <!-- Lazy -->
    <input v-model.lazy="lazy_msg" placeholder="edit me" />
    <br />Press enter for msg to update
    <p>Lazy Message is: {{ lazy_msg }}</p>
    <hr />

    <!-- Number input -->
    <input v-model="msg" placeholder="edit me" />
    <p>Normal Message type is: {{ typeof msg }}</p>
    <input v-model.number="number_msg" placeholder="edit me" />
    <p>Number Message type is: {{ typeof number_msg }}</p>
    <hr />

    <!-- Trim input -->
    <input v-model="msg" placeholder="edit me" />
    <p>Normal Message length is: {{ msg.length }}</p>
    <input v-model.trim="trim_msg" placeholder="edit me" />
    <p>Trim Message length is: {{ trim_msg.length }}</p>
    <hr />
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      message: "",
      lazy_msg: "",
      number_msg: "",
      trim_msg: "",
      msg: "",
    };
  },
  methods: {},
  components: {},
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
