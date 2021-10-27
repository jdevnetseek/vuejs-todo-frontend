<template>
  <div class="container">
    <br />
    <div class="card p-5">
      <h3>Add Todo's</h3>
      <form v-on:submit="addTodo">
        <input type="text" v-model="title" name="title" placeholder="title" class="form-control" />
        <br />
        <textarea
          type="text"
          v-model="description"
          name="title"
          placeholder="description"
          class="form-control"
        />
        <br />
        <input type="submit" value="submit" class="btn btn-primary add-btn" />
      </form>
    </div>
  </div>
</template>
<script>
// import uuid from 'uuid';
// import { v4 as uuidv4 } from 'uuid';
export default {
  name: "AddTodo",
  data() {
    return {
      title: "",
      description: "",
    };
  },
  methods: {
    addTodo(e) {
      e.preventDefault();
      const newTodo = {
        // id:uuidv4(),
        title: this.title,
        description: this.description,
        completed: false,
      };
      // console.log(newTodo)
      this.$emit("add-todo", newTodo);
      this.title = "";
      this.description = "";
    },
  },
};
</script>
<style scoped>
.card{
  box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px, rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px, rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;
}
.add-btn {
  float: left;
}
</style>