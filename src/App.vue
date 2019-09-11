<template>
  <div id="app">

    <div class="container-fluid">
      <div class="row">
        <div class="col-md-2 d-none d-md-block bg-light sidebar">
          <div id="nav">
            <router-link to="/">Home</router-link> |
            <router-link to="/about">About</router-link>
          </div>
        </div>
        <div class="col-md-9 ml-sm-auto col-lg-10 px-4">
          <div class="alert alert-success alert-dismissible fade show" role="alert">
            With Bootstrap!
            <button type="button" class="close" data-dismiss="alert" aria-label="Close">
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <router-view/>
        </div>
      </div>
    </div>

  </div>
</template>

<style lang="scss">
.sidebar {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  z-index: 100;
  box-shadow: inset -1px 0 0 rgba(0, 0, 0, .1);
}
</style>
