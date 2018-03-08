<template>
  <form class="add-post">
    <div class="inputs">
      <input v-model="title" placeholder="enter title"/>
      <input v-model="author" placeholder="enter author"/>
      <input v-model="body" placeholder="enter your post!"/>
      <button type="button" @click="onAdd({title, author, body})">add post</button>
    </div>
  </form>
</template>

<script>
export default {
  name: 'AddPost',
  data () {
    return {
      title: '',
      author: '',
      body: ''
    }
  },
  props: [ 'onAdd' ]
}
</script>
