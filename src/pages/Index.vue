<template>
  <Layout>
    <div class="circle">

    </div>

<div class="menu">
    <div v-for="edge in $page.allContentfulStrony.edges" :key="edge.node.id">
      <g-link :to="edge.node.path"  ><p class='krzywak ruch'  >{{edge.node.nazwa}}</p></g-link>
    </div>
</div>


  </Layout>
</template>
<page-query>
  {
    allContentfulStrony {
      edges {
        node {
          nazwa
          id
          path
          }
        }
      }
  }


</page-query>


<script>
export default {
  metaInfo: {
    title: 'Fundacja'
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
