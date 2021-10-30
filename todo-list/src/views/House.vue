<template>
  <div class="container">
    <div class="container1">
      <h1>MY TO-DO LIST</h1>
      <div class="forms">
        <input
          name="name"
          class="textName"
          type="text"
          placeholder="Enter to search..."
          autocomplete="Enter to search..."
          style="text-align: center"
        />
        <button type="submit" class="btnSubmit">Add item</button>
      </div>

      <!-- mới nè -->
      <!--     <div class="todo-list">
          <ul>
              <li>
              <button v-for="todo in todos" :key="todo.id">
                  {{ todo.title }}
                  </button>
              </li>
          </ul>
      </div> -->

      <div class="groupTitle">
        <div class="btn-group" role="group" aria-label="Basic example">
          <button type="button" class="btnTitle" data-toggle="modal" data-target="#myModal">Title</button>
            <div class="modal fade" id="myModal" role="dialog">
              <div class="modal-dialog">
                      <!-- Modal content-->
      <div class="modal-content" style="width: 600px;height: 500px; margin-top:100px;">
        <div class="modal-header">
          <!-- <button type="button" class="close" data-dismiss="modal">&times;</button> -->
          <h1>Title</h1>
        </div>
        <div class="modal-body">
          <div class="form-check">
        <input
          class="form-check-input"
          type="radio"
          name="flexRadioDefault"
          id="flexRadioDefault1"
        />
        <label class="form-check-label" for="flexRadioDefault1"> Item 1 </label>
      </div>
      <div class="form-check">
        <input
          class="form-check-input"
          type="radio"
          name="flexRadioDefault"
          id="flexRadioDefault2"
          checked
        />
        <label class="form-check-label" for="flexRadioDefault2"> Item 2 </label>
      </div>
      <div class="form-check">
        <input
          class="form-check-input"
          type="radio"
          name="flexRadioDefault"
          id="flexRadioDefault1"
        />
        <label class="form-check-label" for="flexRadioDefault1"> Item 3 </label>
      </div>
      <div class="form-check">
        <input
          class="form-check-input"
          type="radio"
          name="flexRadioDefault"
          id="flexRadioDefault1"
        />
        <label class="form-check-label" for="flexRadioDefault1"> Item 4 </label>
      </div>
        </div>
        <div class="modal-footer">
          <button type="button" class="btnClose" data-dismiss="modal">Close</button>
        </div>
      </div>
      
    </div>
  </div>
          <button class="btnEdit" data-toggle="modal" data-target="#myModal1">
            <!-- Modal -->
  <div class="modal fade" id="myModal1" role="dialog">
    <div class="modal-dialog">
    
      <!-- Modal content-->
      <div class="modal-content">
        <div class="modal-header">
          <button type="button" class="close" data-dismiss="modal">&times;</button>
          <h4 class="modal-title">Modal Header</h4>
        </div>
        <div class="modal-body">
          <p>Some text in the modal.</p>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
        </div>
      </div>
      
    </div>
  </div>
            <i class="fas fa-edit"></i>
          </button>
          <button class="btnDelete">
            <i class="fas fa-trash-alt"></i>
          </button>
          <modal: active.sync="isEditModalActive" has-modal-card>
            <todo-edit-modal
        :todo="selectedTodo"
        :priorities="priorities"
        @edit-todo="onEditTodo"
      ></todo-edit-modal>
          </modal:>
        </div>
        <div class="btn-group" role="group" aria-label="Basic example">
          <button type="button" class="btnTitle">Title</button>
          <button class="btnEdit">
            <i class="fas fa-edit"></i>
          </button>
          <button class="btnDelete">
            <i class="fas fa-trash-alt"></i>
          </button>
        </div>
        <div class="btn-group" role="group" aria-label="Basic example">
          <button type="button" class="btnTitle">Title</button>
          <button class="btnEdit">
            <i class="fas fa-edit"></i>
          </button>
          <button class="btnDelete">
            <i class="fas fa-trash-alt"></i>
          </button>
        </div>
        <div class="btn-group" role="group" aria-label="Basic example">
          <button type="button" class="btnTitle">Title</button>
          <button class="btnEdit">
            <i class="fas fa-edit"></i>
          </button>
          <button class="btnDelete">
            <i class="fas fa-trash-alt"></i>
          </button>
        </div>
        <div class="btn-group" role="group" aria-label="Basic example">
          <button type="button" class="btnTitle">Title</button>
          <button class="btnEdit">
            <i class="fas fa-edit"></i>
          </button>
          <button class="btnDelete">
            <i class="fas fa-trash-alt"></i>
          </button>
        </div>
      </div>
      <!-- <div id="app"></div> -->
      <nav aria-label="...">
  <ul class="pagination justify-content-center">
    <li class="page-item disabled">
      <a class="page-link" href="#" tabindex="-1" aria-disabled="true">Previous</a>
    </li>
    <li class="page-item"><a class="page-link" href="#">1</a></li>
    <li class="page-item active" aria-current="page">
      <a class="page-link" href="#">2 <span class="sr-only">(current)</span></a>
    </li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
    <li class="page-item">
      <a class="page-link" href="#">Next</a>
    </li>
  </ul>
</nav>

</div>
  </div>
</template>
<script>
/* import Title from "@/components/Title.vue" */
/* Vue.component("paginate", VuejsPaginate);

new Vue({
  el: "#app",
  template: `
    <paginate 
      :pageCount="10"
      :containerClass="'pagination'"
      :clickHandler="clickCallback">
    </paginate>
  `,
  methods: {
    clickCallback: function (page) {
      console.log(page);
    },
  },
}); */
export default {
  /*  name: "home",
  components :{Title},
  data() {
    return {
      isEditModalActive: false,
    }
  }, */
  /* /*   methods() {
    openEditModal() {
      this.selectedTodo = todo;
      this.isEditModalActive = true;
    },
    onEditTodo(item) {
      const todo = this.findTodo(item);
      // Apply the updated values
      todo.todo = item.todo;
      todo.priority = item.priority;
      // save the updated array in localstorage
      this.saveLocalStorageTodos();
      // close the modal
      this.isEditModalActive = false;
    }, */
};

/*     name: 'Todos',
    data() {
        return {
            todos: [
                { id: 1, title: 'Tittle', completed: false },
                { id: 2, title: 'Tittle', completed: false },
                { id: 3, title: 'Tittle', completed: false },
                { id: 4, title: 'Tittle', completed: false },

            ]
        }
    } 
}; */
</script>
<style scoped>
/* sửa từ đây nữa */
/* .todo-list ul {
	padding: 0 10px 10px 10px;
	list-style-type: none;
}

.todo-list li {
	padding: 10px;
	cursor: pointer;
	margin: 10px 0;
	border-radius: 4px;
	background: rgb(240, 240, 240);
	color: black;
}
.todo-list li.completed {
	background: rgb(119, 218, 243);
}

.todo-list li button {
	float: right;
	margin-right: 20px;
}

.todo-list li button:hover {
	cursor: pointer;
	background: red;
	color: white;
}
.todo-list {
    padding-top: 20px;
} */
/*  */

h1 {
  margin-left: 20px;
  font-weight: 900;
}
.container1 {
  background: white;
  padding: 30px 0 50px 0;
  width: 900px;
  margin: auto;
  height: 500px;
}
.container {
  width: 100%;
  height: 100vh;
  overflow: hidden;
  padding-top: 100px;
  background-color: rgb(221, 233, 241);
}
.forms {
  float: right;
  margin-right: 20px;
  margin-top: -30px;
}
.btnSubmit {
  background-color: rgb(37, 201, 22);
  margin-left: 20px;
  width: 80px;
  height: 25px;
}
.textName {
  height: 30px;
  width: 200px;
}
.btnTitle {
  width: 90%;
  text-align: left;
  border: none;
  background-color: white;
}
.btn-group {
  width: 95%;
  border: groove;
}
.btnEdit {
  background-color: white;
  border: none;
  height: 30px;
}
.btnDelete {
  background-color: white;
  border: none;
}
.groupTitle {
  margin-top: 20px;
  width: 100%;
  margin-left: 20px;
}
.btnClose {
    background-color: aqua;
    text-align: center;
    width:100vh;
    margin-right: 200px;
    margin-left: 200px;
    border-top-right-radius: 10px;
    border-bottom-left-radius: 10px;
    border-top-left-radius: 10px;
    border-bottom-right-radius: 10px;
}
</style>

