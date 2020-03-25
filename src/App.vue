<template>
  <div class="container">
    <add-todos />
    <Todos />
  </div>
</template>

<script>
const Todos = resolve => {
  require.ensure(
    ['./components/Todos'],
    () => {
      resolve(require('./components/Todos'));
    },
    'user'
  );
};
import AddTodos from './components/AddTodo';

export default {
  name: 'App',
  components: {
    Todos,
    addTodos: AddTodos
  }
};
</script>

<style>
body {
  color: aliceblue;
  font-family: 'Baloo Da 2';
  font-size: 1.3;
  line-height: 1.6;
  background: #222222;
}
.container {
  max-width: 1100px;
  margin: auto;
  overflow: auto;
  padding: 0 2rem;
}
</style>
