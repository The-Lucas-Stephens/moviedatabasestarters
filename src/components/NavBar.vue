<template>
   <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Navbar</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <!-----<a class="nav-link active" aria-current="page" href="#">Home</a>-->
          <router-link to="/movies" class="nav-link">Movies</router-link>
        </li>
        <li class="nav-item">
          <!-----<a class="nav-link active" aria-current="page" href="#">Home</a>-->
          <router-link to="/" class="nav-link">Home</router-link>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Features</a>
        </li>
       
      </ul>
    </div>
  </div>
</nav>
</template>

<script>
export default{
    name: "NavBar"
}
</script>
<style scoped>
    .nav-link {padding: 25px;}
</style>
