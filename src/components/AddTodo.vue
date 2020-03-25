<template>
  <div>
    <h3>Add Todo :</h3>
    <div class="add">
      <form>
        <input type="text" v-model.lazy="title" placeholder="Add Todo..." />
        <input type="submit" value="Add Item" />
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: ''
    };
  },
  name: 'AddTodo'
};
</script>

<style scoped>
form {
  display: flex;
}
input {
  border-radius: 4px;
}
input[type='text'] {
  flex: 10;
  background: #181a1b;
  padding: 10px;
  border: 1px solid grey;
  outline: 0;
  color: whitesmoke;
}
input[type='submit'] {
  flex: 2;
  background: rgb(228, 187, 4);
  font-weight: bolder;
  font-size: 1.4rem;
  color: black;
  cursor: pointer;
  border: 1px solid grey;
}
</style>
