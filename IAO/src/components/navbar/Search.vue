<template>
  <li class="nav-item">
    <div v-on:mouseover="expandSearch" class="search-btn nav-link">
      <slot />
      <span class="link-text">{{ navText }}</span>
    </div>
    <div class="search-overlay">
      <div class="search-popup">
        <form class="search-form">
          <div class="form-group">
            <input
              class="form-control"
              placeholder="Start Typing"
              type="text"
            />
            <button @click="collapseSearch" class="close-btn">FECHAR</button>
          </div>
        </form>
      </div>
    </div>
  </li>
</template>

<script>
export default {
  props: {
    navText: {
      required: true,
      type: String,
    },
  },
  methods: {
    expandSearch() {
       
      const input = document.querySelector(".search-btn");
      const searchOverlay = document.querySelector(".search-overlay");
      
      input.addEventListener("click",()=>{
           searchOverlay.classList.add("active");

        });
     
    },
    collapseSearch() {
        const searchOverlay = document.querySelector(".search-overlay");
        searchOverlay.addEventListener("click",(event)=>{
            searchOverlay.classList.remove("active");
        })
    },
  },
};
</script>

<style src="~/assets/navbar/navbar.css" />