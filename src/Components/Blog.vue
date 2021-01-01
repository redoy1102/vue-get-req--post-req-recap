<template>
  <div>
    <div class="Blog" v-for="(blog,id) in blogs" :key="id">
      <h1>Id: {{blog.id}}</h1>
      <h3>Title: {{blog.title}}</h3>
      <p><b>Description:</b> {{ blog.body }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      blogs: []
    }
  },
  created() {
    this.$http.get('https://jsonplaceholder.typicode.com/posts')
        .then((data) => {

          this.blogs = data.body.slice(0, 10);
        })
  }
}
</script>

<style scoped>
.Blog {
  border: 2px solid Black;
  text-align: center;
  padding: 10px 0px 10px 0px;
  margin-top: 5px;
}
</style>