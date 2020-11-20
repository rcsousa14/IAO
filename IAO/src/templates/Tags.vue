<template>
  <Layout>
    <h1>{{ $page.tags.id }}</h1>
    <pre>
        {{$page.tags}}
    </pre>
  </Layout>
</template>

<page-query>
query tags($id: ID!){
  tags(id: $id){
    id
    belongsTo {
      edges {
        node{
          ...on Documentation {
            title
          }
        }
      }
    }
  }
}
</page-query>

<script>
export default {};
</script>

<style>
</style>