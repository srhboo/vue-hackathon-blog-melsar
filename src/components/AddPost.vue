<template>
  <form class="add-post">
    Add Post:
    <input v-model="title"/>
    <input v-model="author"/>
    <input v-model="body"/>
    <button type="button" @click="onAdd({title, author, body})"/>
  </form>
</template>

<script>
export default {
  name: 'AddPost',
  data () {
    return {
      title: 'hello',
      author: 'enter',
      body: 'body'
    }
  },
  props: [ 'onAdd' ]
}
</script>
