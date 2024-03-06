<template>
  <div class="container">
    <h1 class="header">Todo List</h1>
    <div id="newtask" class="inputDiv">
      <input
        ref="myInput"
        type="text"
        class="todoInput"
        v-model="model"
        placeholder="Add Tasks"
        @keydown.enter="addTask"
      />
      <button @click="addTask" class="addTaskBtn" id="push">Add Task</button>
    </div>
    <div id="tasks"></div>
    <ul class="buttonUl">
      <li class="" v-for="(item, index) in data" :key="index">
        <div class="items flex justify-between items-center">
          <span :class="{strike:item.completed}" class="itemText flex-1 text-left">{{ item.text }}</span>
          <div class="btngroup items-end">
            <button @click="doneTask(item)" type="button" class="btn done bg-green-500">Done</button>
            <button @click="deleteTask(index)" type="button" class="btn delete bg-red-500">Delete</button>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Todo",
  data() {
    return {
      model: "",
      data: [],
    };
  },
  methods: {
    addTask() {
      if (this.model !== "") {
        this.data.push({
          id: Date.now(),
          text: this.model,
          completed: false,
        });
      }
      //To empty input field
      this.model= '';
      //for focus in input field
      this.$refs.myInput.focus();
    },
    deleteTask(index){
      this.data.splice(index,1);
      this.$refs.myInput.focus();
    },
    doneTask(item){
      const idx = this.data.findIndex((x)=>x.id === item.id);
      this.data[idx].completed =!item.completed;
      this.$refs.myInput.focus();
    },
  },
};
</script>

<style scoped>
/* Fonts */
@import url("https://fonts.googleapis.com/css2?family=Anta&display=swap");

/* Reset */
*,
*:before,
*:after {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.strike{
  text-decoration: line-through;
}
.btn {
  padding: 3px 5px;
  margin: 5px;
  border-radius: 3px;
  color: white;
  border: none;
  font-size: 12px;
}
.done {
  margin-left: 20px;
}
.itemText {
  text-transform: capitalize;
  padding-left: 10px;
  font-size: 12px;
}

.items {
  border: 1px solid #ddd;
  padding: 5px;
  margin: 10px;
  border-radius: 5px;
}
.



/* Typography */
body {
  font-family: "Anta", sans-serif;
  font-weight: 400;
  font-style: normal;
}

/* Layout */
.container {
  width: 45%;
  min-width: 60%;
  min-height: 100px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: white;
  border-radius: 10px;
}

/* Input and Button */
#newtask {
  padding: 10px 20px;

}

#newtask input {
  width: 75%;
  height: 45px;
  padding: 12px;
  color: #111111;
  font-weight: 500;
  border-radius: 5px;
  border: 2px solid #d1d3d4;
  font-family: "Poppins", sans-serif;
  font-size: 15px;
}

#newtask input:focus {
  outline: none;
  border-color: #0d75ec;
}

#newtask button {
  float: right;
  width: 20%;
  height: 45px;
  font-weight: 500;
  font-size: 16px;
  background-color: #0d75ec;
  border: none;
  color: #ffffff;
  cursor: pointer;
  outline: none;
  border-radius: 5px;
}

/* Tasks */
#tasks {
  width: 100%;
  padding: 30px 20px;
  margin-top: 10px;
  background-color: #ffffff;
  border-radius: 10px;
}

.task {
  display: flex;
  align-items: center;
  justify-content: space-between;
  border: 1px solid #939697;
  background-color: #c5e1e6;
  height: 50px;
  margin-bottom: 8px;
  padding: 5px 10px;
  border-radius: 5px;
  cursor: pointer;
}

.task span {
  font-family: "Anta", sans-serif;
  font-weight: 400;
  font-style: normal;
}

.task button {
  width: 40px;
  height: 100%;
  background-color: #6583e5;
  color: #ffffff;
  border: none;
  cursor: pointer;
  outline: none;
  border-radius: 5px;
  font-family: "Anta", sans-serif;
}
</style>
