<template>
  <div class="layout">
   
    <nav class="navbar">
        <ul class="navbar-nav">
            <Logo />
            <NavItems nav-text="Tutoriais" to="/About">
              <Tutorial />
            </NavItems>
            <NavItems nav-text="Hastags">
              <Tags />
            </NavItems>
            <NavItems nav-text="Pesquisa">
              <Search />
            </NavItems>
             <NavItems nav-text="Modo">
              <Theme />
            </NavItems>
           
        </ul>
    </nav>
    <slot/>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
import Logo from "~/components/navbar/Logo.vue"
import NavItems from "~/components/navbar/NavItems.vue"
import Tutorial from "~/assets/svgs/tutorial.svg"
import Tags from "~/assets/svgs/tags.svg"
import Search from "~/assets/svgs/search.svg"
import Theme from "~/assets/svgs/theme.svg"
export default {
  components:{
    Logo,
    NavItems,
    Tutorial,
    Tags,
    Search,
    Theme
  
 
  }
}
</script>

<style src="~/assets/navbar/navbar.css" />




