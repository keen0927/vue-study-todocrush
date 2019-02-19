<template>
    <div class="todo-item" :class="{'is-complete':todo.completed}">
        <p>{{todo.title}}</p>
    </div>
</template>

<script>
  export default {
    name: 'TodoItem',
    props: ["todo"]
  }
</script>

<style scoped>
.todo-item {
    background: #f4f4f4;
    padding: 10px;
    border-bottom: 1px solid #ccc;
}
    .is-complete {

        text-decoration: line-through;

    }
</style>
