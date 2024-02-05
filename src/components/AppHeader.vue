<script>
export default {
    data() {
      return {
        navLinks: [
          {
            name: 'Home',
            routeName: 'home'
          },
          {
            name: 'About us',
            routeName: 'about'
          },
        ],
      }
    }
}
</script>

<template>
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Boolfolio</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
      <div class="navbar-nav">
        <li v-for="link in navLinks" :key="link.name">
          <router-link :to="{ name: link.routeName }" class="nav-link">{{ link.name }}</router-link>
        </li>
      </div>
    </div>
  </div>
</nav>
</template>

<style lang="scss" scoped></style>