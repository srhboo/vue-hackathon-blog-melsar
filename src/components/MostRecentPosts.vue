<template>
  <div class="posts">
    <AddPost :onAdd="onAddPost"/>
    <ul>
      <li v-for="post in posts" :key="post.title">
        <BlogPost :title="post.title" :author="post.author" :body="post.body"/>
      </li>
    </ul>
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
        { title: 'Title 1', author: 'author1', body: 'post1' },
        { title: 'Title 2', author: 'author2', body: 'post2' }
      ]
    }
  },
  methods: {
    onAddPost: function (post) {
      this.posts.push(post)
    }
  }
}
</script>
