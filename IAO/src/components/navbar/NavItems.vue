<template>
  <li class="nav-item">
    <g-link :to="to" class="nav-link">
       <slot/>
      <span class="link-text">{{navText}}</span>
    </g-link>
    
    
   
  </li>
 
</template>

<script>

export default {
    
    
    props:{
      to:{
        // required: true,
        type: String
      },
      navText:{
        required: true,
        type: String
      }
    }
      
      
      
};
</script>

<style src="~/assets/navbar/navbar.css" />