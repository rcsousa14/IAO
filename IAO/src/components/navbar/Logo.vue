<template>
  <li class="logo">
     <g-link to="/" class="nav-logo">
        <Logo />
     </g-link>
    
  </li>
</template>

<script>
import Logo from "~/assets/svgs/logo.svg"
export default {
  components:{
    Logo
  }
};
</script>

<style src="~/assets/navbar/navbar.css" />