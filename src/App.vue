<template>
  <div id="app">
    <Todos v-bind:todos="todos" />
      <Input v-model="value" placeholder="Enter something..." style="width: 300px" />
      <Input v-model="value1" size="large" placeholder="large size" />
      <br>
      <Input v-model="value2" placeholder="default size" />
      <br>
      <Input v-model="value3" size="small" placeholder="small size" />
  </div>
</template>

<script>
import Todos from './components/Todos';

export default {
  name: 'app',
  components: {
    Todos
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "Todo One",
          completed: false
        },
        {
          id: 2,
          title: "Todo Two",
          completed: true
        },
        {
          id: 3,
          title: "Todo Three",
          completed: false
        }
      ]
    }
  }
}
</script>

<style>
</style>
