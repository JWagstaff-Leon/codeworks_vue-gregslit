<template>
    <nav class="navbar navbar-dark navbar-expand bg-dark text-light no-select">
        <div class="selectable h-100" data-bs-toggle="offcanvas" data-bs-target="#listings-menu">
            <span class="mx-2">Gregs'List<span id="title-suffix"></span></span>
        </div>
            <Login />
    </nav>
</template>

<script>
export default {
  setup() {
    return {};
  },
};
</script>

<style scoped>
a:hover {
  text-decoration: none;
}
.nav-link {
  text-transform: uppercase;
}
.navbar-nav .router-link-exact-active {
  border-bottom: 2px solid var(--bs-success);
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
}
</style>
