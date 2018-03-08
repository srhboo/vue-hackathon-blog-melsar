<template>
  <div class="blog-post">
    <h1>{{ title }}</h1>
    <h4>{{ author }}</h4>
    <div>{{ body }}</div>
  </div>
</template>

<script>
export default {
  name: 'BlogPost',
  props: ['title', 'author', 'body']
}
</script>
