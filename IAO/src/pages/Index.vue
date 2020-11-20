<template>
  <Layout>
    <Thumbnail />
  
        <h1 class="title">Recente</h1>
  
  <Tutorials />
  </Layout>
</template>

<script>
import Thumbnail from "~/components/main/thumbnail/thumb.vue";
import Tutorials from "~/components/main/tutorials/tut.vue";
export default {
  components:{
    Thumbnail,
    Tutorials
  },
  metaInfo: {
    title: 'iao-main'
  }
}
</script>

<style>

</style>
