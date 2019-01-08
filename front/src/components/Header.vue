<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark background-blue-navbar">
    <a class="navbar-brand" href="#">
      <img src="../assets/img/ic_zhuli-logo.svg" width="60" height="60" alt>
    </a>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarSupportedContent"
      aria-controls="navbarSupportedContent"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav ml-auto">
        <li class="navbar-text text-style">
          <h1>Bienvenido</h1>
        </li>
      </ul>
      <ul class="navbar-nav ml-auto profile-style">
        <li class="nav-item dropdown">
          <a
            class="nav-link dropdown-toggle btn-sm "
            href="#"
            id="navbarDropdown"
            role="button"
            data-toggle="dropdown"
            aria-haspopup="true"
            aria-expanded="false"
          >
            <font-awesome-icon icon="bell" size="2x" class="icon-color"/>
          </a>
          <div class="dropdown-menu" aria-labelledby="navbarDropdown">
            <a class="dropdown-item" href="#">Notification 1... 2:00pm</a>
            <div class="dropdown-divider"></div>
            <a class="dropdown-item" href="#">Notification 2... 2:00pm</a>
            <div class="dropdown-divider"></div>
            <a class="dropdown-item" href="#">Notification 3... 2:00pm</a>
          </div>
        </li>
      </ul>
      <ul class="navbar-nav ">
        <a class="nav-item">
          <img class="avatar-style" src="https://avatars2.githubusercontent.com/u/4169949?s=460&v=4" width="60" height="60" alt>
        </a>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Header"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.background-blue-navbar {
  background-color: #191c21 !important;
}
.dropdown-menu {
  background-color: #dbe6ff;
}

.dropdown-menu > li > a {
  color: #191c21;
}
a,
a:focus,
a:hover {
  color: #191c21;
}
.avatar-style {
  border-radius: 50%;
  background-color: #dbe6ff;
}
.profile-style {
  padding-right: 3%;
}
.dropdown-menu {
  left: 50% !important;
  transform: translateX(-50%) !important;
  top: 100% !important;
}
@media screen and (max-width: 768px) {
  .profile-style {
    padding-left: 0;
    padding-right: 0;
  }
}
</style>
