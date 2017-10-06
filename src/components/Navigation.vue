<template>
  <nav class="navbar is-light">
    <div class="navbar-brand">
      <router-link class="navbar-item" to="/">
        <h1 class="subtitle">MPEServer</h1>
      </router-link>

      <div class="navbar-burger burger" data-target="nav">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>

    <div id="nav" class="navbar-menu">
      <div class="navbar-end">
        <router-link class="navbar-item" to="/second">
          Second
        </router-link>
        <router-link class="navbar-item" to="/tabs">
          Tabs
        </router-link>
      </div>
    </div>
  </nav>
</template>

<script>
  export default {
    name: 'navigation'
  }

  document.addEventListener('DOMContentLoaded', function () {
    var $navbarBurgers = Array.prototype.slice.call(document.querySelectorAll('.navbar-burger'), 0);
    if ($navbarBurgers.length > 0) {
      $navbarBurgers.forEach(function ($el) {
        $el.addEventListener('click', function () {
          var target = $el.dataset.target;
          var $target = document.getElementById(target);
          $el.classList.toggle('is-active');
          $target.classList.toggle('is-active');

        });
      });
    }
  })
</script>

<style scoped>
  .navbar {
    box-shadow: 0px 0px 1px 1px rgba(43, 43, 43, 0.63);
  }
</style>
