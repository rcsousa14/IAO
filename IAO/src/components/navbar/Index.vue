<template>
  <nav class="navbar">
      <ul class="navbar-nav">
        <Logo />
        <NavItems nav-text="Tutoriais" to="/tutoriais">
          <Tutorial />
        </NavItems>
        <NavItems nav-text="Snippets" to="/trechos">
          <Code />
        </NavItems>
        <NavItems nav-text="Hastags" to="/tags">
          <Tags />
        </NavItems>
        <NavSearch nav-text="Pesquisa">
          <Search />
        </NavSearch>
        <NavItems nav-text="Modo">
          <Theme />
        </NavItems>
      </ul>
    </nav>
</template>

<script>
import Logo from "~/components/navbar/Logo.vue";
import NavItems from "~/components/navbar/NavItems.vue";
import Tutorial from "~/assets/svgs/tutorial.svg";
import Tags from "~/assets/svgs/tags.svg";
import Search from "~/assets/svgs/search.svg";
import Code from "~/assets/svgs/snippets.svg";
import Theme from "~/assets/svgs/theme.svg";
import NavSearch from "~/components/navbar/Search.vue"
export default {
components: {
    Logo,
    NavItems,
    Tutorial,
    Tags,
    Search,
    Theme,
    Code,
    NavSearch
  },
}
</script>

<style src="~/assets/navbar/navbar.css" />