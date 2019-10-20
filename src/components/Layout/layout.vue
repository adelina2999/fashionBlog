<template>
  <div class="container">
    <h1 v-if="number<6">{{title}}</h1>
    {{message}}
  <ol>
    <li v-for="todo in todos"
      :key="todo.id">
      {{ todo.name }} {{ todo.text }}
    </li>
  </ol>
  </div>
</template>

<script>
export default {
  name: 'Layout',
  data () {
    return {
      title: 'Layout',
      message: 'You loaded this page on ' + new Date().toLocaleString(),
      number: 5,
      todos: [{
        name: 'toRun',
        text: 'I must run 10 km'
      },
      {
        name: 'toEat',
        text: 'Vadim is hungry'
      }]
    }
  },
  created () {
    console.log(this.title)
  }
}
</script>
