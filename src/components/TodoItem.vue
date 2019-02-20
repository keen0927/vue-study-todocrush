<template>
    <div class="todo-item" :class="{'is-complete':todo.completed}">
        <p>
            <Checkbox @change="markComplete">{{todo.title}}</Checkbox>


        </p>
    </div>
</template>

<script>
  export default {
    name: 'TodoItem',
    props: ["todo"],
    methods: {
      markComplete() {
        this.todo.completed = !this.todo.completed;
      }
    }
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
