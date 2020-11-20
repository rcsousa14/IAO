<template>
  <section class="grid-container">
    <div
      class="grid-item"
      v-for="edge in $static.docs.edges"
      :key="edge.node.id"
    >
      <div class="card">
        <g-link :to="edge.node.path">
          <img :src="edge.node.featuredImage" alt="W3Schools.com" />
        </g-link>
        
        <div class="card-body">
          <div class="card-row">

           
             <g-link class="tag" v-for="tag in edge.node.tags" :key="tag.id" :to="tag.path"
            :style="`background: ${tag.color}`"
              >#{{ tag.id }}</g-link
            >
           
            
          </div>
          <h4>{{ edge.node.title }}</h4>
          <p>
            {{ edge.node.description }}
          </p>
          <div class="card-small">
            <small>{{ edge.node.read }}</small>

            <small>{{ edge.node.date }}</small>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<static-query>
  query documentation {
    docs: allDocumentation {
      edges {
        node {
          title
          description
          read
          date
          path
          featuredImage
          tags{
            id
            color
            path
          }
        }
      }
    }
  }
</static-query>
<script>
export default {};
</script>

<style>
.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(20rem, 1fr));
  padding: 0.5rem;
  margin-bottom: 2rem;
  gap: 0.5rem 0.5rem;
}
.grid-item {
  box-shadow: 0 2px 20px rgb(0, 0, 0, 0.1);
  max-width: 27rem;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  -moz-osx-font-smoothing: grayscale;
  -webkit-transition-duration: 0.3s;
  transition-duration: 0.3s;
  -webkit-transition-property: transform;
  transition-property: transform;
  -webkit-transition-timing-function: ease-out;
  transition-timing-function: ease-out;
  display: inline-block;
  vertical-align: middle;
  -webkit-transform: translateZ(0);
  transform: translateZ(0);
  background-color: white;
}

.grid-item:hover {
  
  -webkit-transform: translateY(-8px);
  transform: translateY(-8px);
}

.card {
  background-color: white;
  overflow: hidden;
  border-radius: 0.19rem;
  text-decoration: none;
}

.card img {
  width: 100%;
  height: 15rem;
  object-fit: cover;
  background-color: grey;
}

.card-body {
  background-color: white;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 1rem 1rem 1.5rem 1rem;
  max-height: 14rem;
}

.card-row {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
}

.card-small {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 100%;
  color: #000;
}

.card-small small {
  font-weight: bold;
}

.tag {
  font-size: 12px;
  font-weight: 500;
  color: white;
  margin: 0.14rem;
  text-transform: uppercase;
  padding: 0.3rem;
  border-radius: 0.15rem;
  text-decoration: none;
}

.card-body h4 {
  font-size: 22px;
  margin: 10px 0;
  color: #000;
}

.card-body p {
  margin: 0 0 40px 0;
  color: rgb(70, 68, 68);
}
@media only screen and (max-width: 600px) {
  .grid-item {
    box-shadow: 0 2px 20px rgb(0, 0, 0, 0.1);
    max-width: 100%;
  }
}
</style>