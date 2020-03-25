<template>
  <div>
    <h1>TODOs</h1>
    <div class="todos">
      <div v-for="todo in allTodos" :key="todo.id" class="todo">
        {{ todo.title }}
      </div>
    </div>
  </div>
</template>

<script>
import { mapGetters, mapActions } from 'vuex';

export default {
  name: 'Todos',
  computed: { ...mapGetters(['allTodos']) },
  methods: {
    ...mapActions(['fetchTodos'])
  },
  created() {
    this.fetchTodos();
  }
};
</script>

<style scoped>
.todos {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 1.5rem;
}
.todo {
  color: whitesmoke;
  /* background: rgba(212, 176, 16, 0.644); */
  font-weight: bolder;
  border: 1px solid #ccc;
  background: #35393c;
  padding: 1rem;
  border-radius: 5px;
  text-align: center;
  position: relative;
  cursor: pointer;
}
</style>
