<template>
  <div>
    <h1>{{ $page.tag.title }}</h1>
  </div>
</template>

<page-query>
query ($id: ID!) {
  tag: strapiTag (id: $id) {
    id
    title
    posts {
      id
      title
    }
  }
}
</page-query>

<script>
export default {
  name: 'TagPage'
}
</script>

<style></style>
