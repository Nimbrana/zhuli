<template>
  <div class="container-fluid">
    <div class="menu-content">
      <div class="card-group">
        <div
          v-for="(menu,key) in Menu"
          v-bind:item="menu"
          v-bind:index="key"
          v-bind:key="key"
          class="card text-center"
          v-on:mouseover="mouseOver(menu.name)"
          v-on:mouseleave="mouseOver(' ')"
        >
          <div class="card-body">
            <h3 class="card-title">{{menu.title}}</h3>
          </div>
          <img class="card-img-bottom" :src="menu.image" alt="Card image cap">
        </div>
      </div>
    </div>
    <div class="container-fluid">
      <h1 id="hello" ref="hello" style="text-align: center;">{{name}}</h1>
    </div>
  </div>
</template>

<script>
import MenuJson from "../assets/data/menu.json";
import Vue from "vue";

export default {
  name: "MainContent",
  data() {
    return {
      Menu: MenuJson.menu,
      name: " "
    };
  },
  methods: {
    mouseOver: function(n) {
      this.name = n;
      /* eslint-disable no-alert, no-console */
      console.log("flag " + this.name);
    }
  }
};
Vue.filter("truncate", function(text, stop, clamp) {
  return text.slice(0, stop) + (stop < text.length ? clamp || "..." : "");
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.menu-content {
  margin-top: 5%;
  margin-bottom: 2%;
  background-color: #dbe6ff;
}
.card {
  border: none !important;
  background-color: #dbe6ff;
  padding: 3%;
}
.card:hover {
  background-color: rgba(102, 163, 217, 0.36);
}
.container-fluid {
  padding: 0 !important;
}
.card-group {
  padding-right: 9%;
  padding-left: 9%;
}
</style>
