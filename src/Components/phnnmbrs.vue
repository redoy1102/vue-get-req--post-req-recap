<template>
  <div>
    <div id="phone" class="phnnmbrs" v-for="(people,id) in peoples" :key="id">
      <h3>Name: {{ people.phone }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      peoples: []
    }
  },
  created() {
    this.$http.get('https://jsonplaceholder.typicode.com/users')
        .then((data) => {
          this.peoples = data.body.slice(0, 10)
        })
  }
}
</script>

<style scoped>

.phnnmbrs {
  border: 2px solid red;
  text-align: center;
  padding: 10px 0px 10px 0px;
  margin-top: 5px;
  width: 50%;
}

</style>