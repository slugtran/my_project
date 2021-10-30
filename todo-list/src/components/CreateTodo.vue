<template>
  <div class="row justify-content-between">
  <form class="col-4" @submit.prevent="addTodo()">
    <input
      v-model="newTodo"
      type="text"
      style="float: left;
      text-size: 24px;
      width: 80%"
      class="form-control"
      placeholder="Enter to search..."
    />
    <span class="btn btn-primary" type="submit" style="float: right; width:20%" @click="isAddModalActive = true">Add new</span>
  </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newTodo: ""
    };
  },
  methods: {
    addTodo() {
      if (this.newTodo.length > 0) {
        this.$emit("on-new-todo", this.newTodo);
      }
      this.newTodo = "";
    }
  }
};
</script>

<style lang="scss" scoped></style>