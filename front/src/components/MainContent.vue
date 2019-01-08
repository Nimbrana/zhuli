<template>
  <div class="container-fluid">
    <div class="menu-content">
      <div class="card-group">
        <div class="card text-center" v-on:mouseover="mouseOver('Robin')" v-on:mouseleave="mouseOver(' ')">
          <div class="card-body">
            <h3 class="card-title">Tareas</h3>
          </div>
          <img class="card-img-bottom" src="../assets/img/ic_robin.svg" alt="Card image cap">
        </div>
        <div class="card text-center" v-on:mouseover="mouseOver('Scriba')" v-on:mouseleave="mouseOver(' ')">
          <div class="card-body">
            <h3 class="card-title">Notas</h3>
          </div>
          <img class="card-img-bottom" src="../assets/img/ic_scriba.svg" alt="Card image cap">
        </div>
        <div class="card text-center" v-on:mouseover="mouseOver('Wan shi tong')" v-on:mouseleave="mouseOver(' ')">
          <div class="card-body">
            <h3 class="card-title">Wiki</h3>
          </div>
          <img class="card-img-bottom" src="../assets/img/ic_wan-shi-tong.svg" alt="Card image cap">
        </div>
        <div class="card text-center" v-on:mouseover="mouseOver('Chad')" v-on:mouseleave="mouseOver(' ')">
          <div class="card-body">
            <h3 class="card-title">Chat</h3>
          </div>
          <img class="card-img-bottom" src="../assets/img/ic_chad.svg" alt="Card image cap">
        </div>
      </div>
    </div>
    <div  class="container-fluid">
      <h1 id="hello" ref="hello" style="text-align: center;">{{name}}</h1>
    </div>
  </div>

</template>

<script>
export default {
  name: "MainContent",
  data() {
    return {
        name : " "
    }
  },
  methods: {
    mouseOver: function(n) {
      this.name = n;
      /* eslint-disable no-alert, no-console */
      console.log("flag " + this.name);
    }
  }
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.on {color: green !important;}

.off {color: red !important;}
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
