<template>
  <div>
    <div v-bind:key="todo.id" v-for="todo in todos">
      <h3>{{todo.title}}</h3>
      <Todoitem v-bind:todo="todo" v-on:del-todo="$emit('del-todo', todo.id)" />
    </div>
  </div>
</template>

<script>
import Todoitem from "./Todoitem.vue";

export default {
  name: "Todos",
  props: ["todos"],
  components: {
    Todoitem
  },
  props: ["todos"]
};
</script>

<style scoped>
</style>
