/*
<template>
  <div class="container">
    <div class="container1">
      <h1>MY TO-DO LIST</h1>
      <div class="forms">
        <input
          name="name"
          class="textName"
          type="text"
          placeholder="Enter to search"
          autocomplete="Enter to search"
        />
        <button type="submit" class="btnSubmit">Add item</button>
      </div>
      <ul class="nav nav-pills nav-justified">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Title</a>
        </li>
        <li class="nav-item">
          <button @click="startEditing()" class="btn btn-outline-primary">
            Edit
          </button>
        </li>
        <li class="nav-item">
          <button
            @click="$emit('on-delete')"
            class="btn btn-outline-danger ml-2"
          >
            Delete
          </button>
        </li>
      </ul>
    </div>
    <nav aria-label="Page navigation example">
      <ul class="pagination justify-content-center">
        <li
          class="page-item"
          v-bind:class="{ disabled: currPage === 1 }"
          @click.prevent="setPage(currPage - 1)"
        >
          <a class="page-link" href="">Prev</a>
        </li>
        <li
          class="page-item"
          v-for="n in totalPage"
          v-bind:key="{ active: currPage === n }"
          @click.prevent="setPage(n)"
        >
          <a class="page-link" href="">{{ n }}</a>
        </li>
        <li
          class="page-item"
          v-bind:class="{ disabled: currPage === totalPage }"
          @click.prevent="setPage(currPage + 1)"
        >
          <a class="page-link" href="">Next</a>
        </li>
      </ul>
    </nav>
    <div class="linker">Copyright @2019</div>
  </div>
</template>

<script></script>

<style scoped>
h1 {
  text-align: center;
}
.container {
  padding-top: 250px;
}
.container1 {
  background: rgb(247, 247, 228);
  padding: 25px 0 50px 0;
}
.btnSign {
  text-align: center;
  text-decoration: none;
}
.btnSignIn {
  margin-left: 0px;
  margin-top: 12px;
  border-top-right-radius: 10px;
  border-bottom-left-radius: 10px;
  border-top-left-radius: 10px;
  border-bottom-right-radius: 10px;
  border: none #ffff;
  background: rgb(35, 105, 70);
  width: 100%;
}
.btnSignUp {
  margin-top: 12px;
  border-top-right-radius: 10px;
  border-bottom-left-radius: 10px;
  border-top-left-radius: 10px;
  border-bottom-right-radius: 10px;
  border: none #ffff;
  width: 100%;
}
.linker {
  padding-top: 12px;
  text-align: center;
}
hr {
  width: 96%;
  text-align: center;
  border-bottom: 2px solid rgb(229, 233, 29);
  line-height: 0.1em;
  margin: 10px 0 20px;
  padding: 0 10px;
}
h1 {
  float: left;
}
.forms {
  float: right;
}
a {
  text-align: center;
  float: left;
  width: 60%;
}
i {
  text-align: center;
  float: right;
  width: 20%;
}
.list-group {
  padding-top: 100px;
}
.container2 {
  text-align: center;
}
</style>
*/
