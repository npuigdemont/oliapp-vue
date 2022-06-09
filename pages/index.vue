<template>
  <div>
    <b-navbar toogleable="lg">
      <b-navbar-brand href="#">Oil Shop</b-navbar-brand>
          <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-item><NuxtLink to="/">Home</NuxtLink></b-nav-item>
        <b-nav-item><NuxtLink to="/about">About Page</NuxtLink></b-nav-item>
      </b-navbar-nav>
      
    <b-navbar-nav class="ml-auto">
        <b-nav-form>
          <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
          <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
        </b-nav-form>

        <b-nav-item-dropdown text="Lang" right>
          <b-dropdown-item href="#">EN</b-dropdown-item>
          <b-dropdown-item href="#">ES</b-dropdown-item>
          <b-dropdown-item href="#">FR</b-dropdown-item>
          <b-dropdown-item href="#">CAT</b-dropdown-item>
        </b-nav-item-dropdown>

        <b-nav-item-dropdown right>
          <!-- Using 'button-content' slot -->
          <template #button-content>
            <em>User</em>
          </template>
          <b-dropdown-item href="#">Profile</b-dropdown-item>
          <b-dropdown-item href="#">Sign Out</b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>
    </b-collapse>
    <b-nav pills>
      <b-nav-item-dropdown
      id="dorpdown"
      text="Products"
      toogle-class="nav-link"
      right>
          <b-dropdown-item>
            <NuxtLink to="/oils">Oils</NuxtLink>
          </b-dropdown-item>
          <b-dropdown-item>
            <NuxtLink to="/vinaigrettes">Vinaigrettes</NuxtLink>
          </b-dropdown-item>
           <b-dropdown-item>
            <NuxtLink to="/liquors">Liquors</NuxtLink>
          </b-dropdown-item>
      </b-nav-item-dropdown>
    </b-nav>
    </b-navbar>
    <main>
      
      <Carrousell />
    </main>
  </div>
</template>

<script>
import Carrousell from "../components/Carrousell.vue";
export default {
    name: "IndexPage",
    components: { Carrousell }
}
</script>
<style>
/* home route and active route will show in bold as it matches / and /about */
a.nuxt-link-active {
  font-weight: bold;
}
/* exact link will show the primary color for only the exact matching link */
a.nuxt-link-exact-active {
  color: #00c58e;
}

body {
  font-family: system-ui, -apple-system, BlinkMacSystemFont, Segoe UI, Roboto,
    Helvetica Neue, Arial, Noto Sans, sans-serif, Apple Color Emoji,
    Segoe UI Emoji, Segoe UI Symbol, Noto Color Emoji;
  margin: 0;
}

main {
  margin: 0 auto;
  padding: 0 1rem;
  margin-top: 100px;
  max-width: 1280px;
  text-align: center;
}
img {
  margin-bottom: 1rem;
}

ul {
  list-style-type: none;
  padding: 0;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}
li {
  margin: 0 0.5rem;
  padding: 0.25rem;
  font-size: 1.2rem;
}

nav {
  padding: 0 1rem;
}

a,
a:visited {
  text-decoration: none;
  color: inherit;
}

a:hover {
  color: #00c58e;
}


</style>