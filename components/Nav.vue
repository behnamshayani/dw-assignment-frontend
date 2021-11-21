<template>
  <b-navbar sticky toggleable="lg" type="dark" variant="dark" class="header-nav nav-center w-100">
    <b-navbar-toggle target="nav-collapse--menu" style="z-index: 90;" />
    <b-collapse id="nav-collapse--menu" is-nav>
      <b-navbar-nav id="nav-nav" class="custom-dropdown-menus nav-center">
        <b-nav-item to="#" class="p-2">
          Valentine's Gifts
        </b-nav-item>
        <b-nav-item to="#" class="p-2">
          Watches
        </b-nav-item>
        <b-nav-item to="#" class="p-2">
          Jewelery
        </b-nav-item>
        <b-nav-item to="#" class="p-2">
          Watch Bands
        </b-nav-item>
        <b-nav-item to="#" class="p-2">
          Collections
        </b-nav-item>
        <b-nav-item to="#" class="p-2">
          Shop Instagram
        </b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {
}
</script>

<style scoped>

@media (min-width: 961px) {
  .nav-center {
    position: absolute;
    left: 50%;
    transform: translatex(-50%);
  }
}
@media (max-width: 960px) {
  .nav-center {
    width: 50%;
  }
}
.header-nav {
  height: 3.5rem;
  background-color: rgb(0, 8, 28) !important;
}

.navbar-dark .nav-link {
  color: rgb(255, 255, 255);
  font-family: DWFutura,sans-serif;
  letter-spacing: 2.4px;
  text-transform: uppercase;
  font-weight: normal;
  font-size: 13px;
  line-height: 15.6px;
  padding-right: 0.25rem;
  padding-left: 0.25rem;
}

.nav-item.active .nav-link,
.nav-item:hover .nav-link {
  color: rgb(255, 255, 255);
}

.navbar-nav {
  background-color: rgb(0, 8, 28);
}

.navbar-toggler {
  color: rgb(255, 255, 255);
  border-color: rgb(255, 255, 255);
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
