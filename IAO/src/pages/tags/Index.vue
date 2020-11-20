<template>
  <Layout>
    <h1>tags</h1>
    <ul class="flex-container wrap">
      <g-link
        class="flex-item"
        v-for="tag in $page.tag.edges"
        :key="tag.node.id"
        :to="tag.node.path"
      >
        <li :style="`background: ${tag.node.color}; padding: 0.4rem; border-radius: 0.15rem`">#{{ tag.node.id }}</li>
      </g-link>
    </ul>
  </Layout>
</template>
<page-query>
query Tags {
  tag: allTags {
    edges {
      node {
        id
        color
        path
      }
    }
  }
}
</page-query>
<script>
export default {
  metaInfo: {
    title: "About us",
  },
};
</script>

<style>
.flex-container{
   padding: 0;
  margin: 0;
  list-style: none;
  -ms-box-orient: horizontal;
  display: -webkit-box;
  display: -moz-box;
  display: -ms-flexbox;
  display: -moz-flex;
  display: -webkit-flex;
  display: flex;

}
.wrap    { 
  -webkit-flex-wrap: wrap;
  flex-wrap: wrap;
}
.flex-item {
  padding: 0.5rem;
  color: white;
 text-decoration:none;
  font-size: 1.5rem;
  text-align: center;
  text-transform: uppercase;
}
/* .page_tag {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}
.tag_ {
  font-size: 1.5rem;
  font-weight: 500;
  color: white;
  margin: 0.14rem;
  text-transform: uppercase;
  padding: 0.5rem;
  border-radius: 0.15rem;
  text-decoration: none;
} */
</style>
