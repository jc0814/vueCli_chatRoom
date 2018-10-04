<template>
  <div id="app">
      <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <a class="navbar-brand" href="#">Navbar</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item active">
             <router-link class="nav-link" :to ="'/'" >Hello</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" :to ="'Hello2'">Hello2</router-link>
            </li>
          </ul>
        </div>
      </nav>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: "App"
};
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";

</style>
