<template>
  <div class="container">
    <h1>{{title}}</h1>
    <span :title="message">
      Hover your mouse over me for a few seconds too see when you loaded this page
    </span>
    <span v-if="seen">Now you see me</span>
    <div>
      <b-button v-on:click="toogleSeen ()" variant="danger">Button</b-button>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'Layout',
  data () {
    return {
      title: '',
      message: 'You loaded this page on ' + new Date().toLocaleString(),
      seen: true,
      users: []
    }
  },
  created () {
    axios
      .get('https://jsonplaceholder.typicode.com/users')
      .then(response => {
        console.log(response.data)
        this.users = response.data
      })
    console.log(this.title)
    this.title = 'FashionBlog'
  },
  methods: {
    toogleSeen () {
      this.seen = !this.seen
    }
  }
}
</script>
