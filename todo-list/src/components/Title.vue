<template>
  <div
    class=""
    style="
      background: rgb(247, 247, 228);
      padding: 25px 25px 100px 50px;
      margin-left: 500px;
      margin-right: 500px;
      padding-top: 150px;
    "
  >
    <h1>Title</h1>
    <div class="todo">
      <h3>Todo</h3>
      <br />
      <br />
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
    <button class="btnclose">Close</button>
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
h1 {
  text-align: center;
}
h3 {
  width: 20%;
  float: left;
}
.todo {
    padding-left:250px;
    padding-top: 25px;
}
.btnclose {
    background-color: aqua;
    text-align: center;
    width:300px;
    margin-right: 250px;
    margin-left: 250px;
    border-top-right-radius: 10px;
    border-bottom-left-radius: 10px;
    border-top-left-radius: 10px;
    border-bottom-right-radius: 10px;
}
</style>
