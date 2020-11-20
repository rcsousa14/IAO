<template>
  <Layout>
    <h1>{{ $page.docs.title }}</h1>
    <small><strong>Author: </strong>{{ $page.docs.author }}</small>
    <small><strong>Date: </strong>{{ $page.docs.date }}</small>
    <img :src="$page.docs.featuredImage" alt="">
    <span v-for="tag in $page.docs.tags" :key="tag.id">{{ tag.id }}</span>
    <div class="markdown-body">
      <VueRemarkContent />
    </div>
  </Layout>
</template>

<page-query>
  query documentation($id: ID!) {
    docs: documentation(id: $id) {
     title
     author
     date
     featuredImage
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
@import url(https://cdnjs.cloudflare.com/ajax/libs/github-markdown-css/4.0.0/github-markdown.min.css);
.markdown-body {
  box-sizing: border-box;
  min-width: 200px;
  max-width: 1080px;
  margin: 0 auto;
  padding: 45px;
}

@media (max-width: 767px) {
  .markdown-body {
    padding: 15px;
  }
}
</style>