<template>
    <div class="todo-item" v-bind:class="{'is-complete':todo.completed}">
        <p>
            <Checkbox @on-change="markComplete">{{todo.title}}</Checkbox>
            <!--<input type="checkbox" @change="markComplete" />{{todo.title}}-->
            <Button @click="$emit('del-todo',todo.id)" type="error" ghost>삭제</Button>
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
.is-complete label{
    text-decoration: line-through;
}
</style>
