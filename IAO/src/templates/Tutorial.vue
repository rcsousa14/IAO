<template>
  <Layout>
      <h1>{{$page.docs.title}}</h1>
      <small><strong>Author: </strong>{{$page.docs.author}}</small>
      <small><strong>Date: </strong>{{$page.docs.date}}</small>
      <span v-for="tag in $page.docs.tags" :key="tag.id">{{tag.id}}</span>
    <VueRemarkContent />
  </Layout>
</template>

<page-query>
  query documentation($id: ID!) {
    docs: documentation(id: $id) {
     title
     author
     date
     tags{
       id
       color
     }
    }
  }

</page-query>

<script>
export default {};
</script>

<style>
</style>