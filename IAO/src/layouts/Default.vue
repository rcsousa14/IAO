<template>
  <div class="layout">
    <Nav/>
    <main>
      <slot />
    </main>
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
import Nav from "~/components/navbar/Index.vue"
export default {
  components: {
    Nav
  },
};
</script>






