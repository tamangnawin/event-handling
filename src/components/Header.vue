<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <a class="navbar-brand" href="#">Mero Bazaar</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarColor02" aria-controls="navbarColor02" aria-expanded="false" aria-label="Toggle navigation" style="">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarColor02">
    <ul class="navbar-nav mr-auto">
      <li class="nav-item active">
        <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Fashion</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Electronics</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Life Style</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Daily Needs</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Office</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Web & App Solutions</a></a>
      </li>
    </ul>
    <form class="form-inline my-2 my-lg-0">
      <input class="form-control mr-sm-2" type="text" placeholder="Search">
      <button class="btn btn-secondary my-2 my-sm-0" type="submit">Search</button>
    </form>
  </div>
</nav>
</template>

<script>

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .navbar-dark .navbar-nav .nav-link {
      margin-left: 25px;
}

  .bg-dark {
    background-color: #2c3e50!important;
}

.btn-secondary {
    color: #fff;
    background-color: #7df8db66;
    border-color: #297966;
}

.btn-secondary:hover {
    color: #007b5e;
    background-color:  white;
    border-color:#007b5e;
}
</style>
