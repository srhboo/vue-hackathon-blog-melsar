<template>
    <div class="post">
      <h1>{{ title }}</h1>
      <h4>{{ author }}</h4>
      <div>{{ body }}</div>

      <button type="button">edit</button>
      <button type="button" @click="onDelete(id)">delete</button>
    </div>
</template>

<script>
export default {
  name: 'BlogPost',
  props: ['title', 'author', 'body', 'onDelete', 'id']
}
</script>

<style scoped>
  .post {
    border: 3px solid black;
    width: 15em;
    margin-bottom: 3rem;
    margin-left: 3rem;
    padding: 1rem;
  }
</style>
