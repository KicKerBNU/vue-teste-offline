<template>
  <div class="hello">
    <div v-if="isOnline">
      <h1>{{ msg }}</h1>
      <a class="waves-effect waves-light btn btn-large white-text">button</a>
      <div class="row">
        <div class="col s4"></div>
        <div class="col s4">
          <div class="card blue-grey darken-1">
            <div class="card-content white-text">
              <span class="card-title">Teste Materialize</span>
              <p>
                I am a very simple card. I am good at containing small bits of
                information. I am convenient because I require little markup to
                use effectively.
              </p>
            </div>
            <div class="card-action">
              <a href="#">This is a link</a>
              <a href="#">This is a link</a>
            </div>
          </div>
          <div class="col s4"></div>
        </div>
      </div>
      <h3>Installed CLI Plugins</h3>
      <ul></ul>
      <p>Voce esta navegando online</p>
    </div>
    <div v-if="isOffline">
      <div>
        <h1>Voce esta executando o navegador offline</h1>
      </div>
    </div>
  </div>
</template>

<script>
import { VueOfflineMixin } from "vue-offline";
export default {
  name: "HelloWorld",
  mixins: [VueOfflineMixin],
  props: {
    msg: String
  },
  mounted() {},
  computed: {}
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
