<template>
  <Layout>
      <div v-for="edge in $page.events.edges" :key="edge.node.id">
          {{ edge }}
      </div>
  </Layout>
</template>
<page-query>
query {
  events: allEvent {
    edges {
      node {
        id
        title
        description
        price
        date
        duration
        thumbnail
        image
        category
      }
    }
  }
}
</page-query>
<script>
export default {
  metaInfo: {
    title: 'Hello, world!'
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
