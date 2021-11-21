<template>
  <nav class="navbar navbar-expand-lg navbar-dark">
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav mr-auto navbar-center">
        <li class="nav-item">
          <a class="nav-link" href="#">Valentine's Gifts</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Watches</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Jewelery</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Watch Bands</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Collections</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Shop Instagram</a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
}
</script>

<style scoped>
.navbar-nav.navbar-center {
  position: absolute;
  left: 50%;
  transform: translatex(-50%);
}
.navbar {
  height: 3.5rem;
  background-color: rgb(0, 8, 28);
}

.navbar-dark .navbar-nav .nav-link {
  color: rgb(255, 255, 255);
  font-family: DWFutura,sans-serif;
  letter-spacing: 2.4px;
  text-transform: uppercase;
  font-weight: normal;
  font-size: 13px;
  line-height: 15.6px;
}

a {
  display: block;
  position: relative;
  padding: 0.2em 0;
}

a::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 0.1em;
  background-color: rgb(255, 255, 255);
  transition: opacity 300ms, transform 300ms;
  opacity: 1;
  transform: scale(0);
  transform-origin: center;
}

a:hover::after,
a:focus::after {
  transform: scale(1);
}
</style>
