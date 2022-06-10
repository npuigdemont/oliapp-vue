<template>
       <b-navbar toogleable="lg">
      <b-navbar-brand tag="h1" href="#">Oil Shop</b-navbar-brand>
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
</template>

<script>
export default {
    data() {
        return {
            
        }
    }
}
   
</script>

<style scoped>

body {
  font-family: system-ui, -apple-system, BlinkMacSystemFont, Segoe UI, Roboto,
    Helvetica Neue, Arial, Noto Sans, sans-serif, Apple Color Emoji,
    Segoe UI Emoji, Segoe UI Symbol, Noto Color Emoji;
  margin: 0;
}

</style>
