<template>
  <div>
    <AddPost :onAdd="onAddPost"/>
      <div class="posts">
          <BlogPost
            v-for="post in posts"
            :key="post.id"
            :title="post.title"
            :author="post.author"
            :body="post.body"
            :id="post.id"
            :onDelete="onDeletePost"
          />
      </div>
    </div>
</template>

<script>
import BlogPost from './BlogPost'
import AddPost from './AddPost'

export default {
  name: 'MostRecentPosts',
  components: {
    BlogPost,
    AddPost
  },
  data () {
    return {
      posts: [
        { id: 1, title: 'Title 1', author: 'author1', body: 'post1' },
        { id: 2, title: 'Title 2', author: 'author2', body: 'post2' },
        { id: 3, title: 'Title 3', author: 'author3', body: 'post3' }
      ]
    }
  },
  methods: {
    onAddPost: function (post) {
      this.posts.push(post)
    },
    onDeletePost: function (id) {
      console.log(id)
      this.posts = this.posts.filter(post => post.id !== id)
    }
  }
}
</script>

<style>
.inputs{
  display: flex;
  flex-direction: column;
  align-items: center;
}

input {
  height: 1em;
  box-shadow: none;
  border: 2px solid black;
  margin-bottom: 1em;
  padding: 10px;

}

button {
  height: 2em;
  border: 2px solid black;
  color: black;
}

.posts {
  display: flex;
  justify-content: flex-start;
  flex-wrap: wrap;
  padding-top: 5rem;
}
</style>
