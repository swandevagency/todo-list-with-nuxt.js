<template>
  <div>
      <AppHeader/>
      <div class="task-wrapper">
          <div class="add-task-wrapper">
              <div class="add-task-container">
                  <div class="add-task">
                      <p>Add your Task</p>
                      <button  v-on:click="isHidden = !isHidden" class="new-task">
                          <span v-if="isHidden">New Task</span>
                          <span v-if="!isHidden">Cancle</span>
                      </button>
                  </div>
                  <form v-if="!isHidden" class="display-adding-task" @submit.prevent="addNewTask()">
                      <div class="tasks-wrapper">
                        <input type="text" v-model="title" name="task-title" id="task-title" placeholder="Title">
                        <input type="text" v-model="description" name="task-description" id="task-description" placeholder="Description">
                      </div>
                      <div class="tasks-button-wrapper">
                          <span v-if="error">{{error}}</span>
                        <input type="submit" value="Add Task" id="task-button">
                      </div>
                  </form>
              </div>
          </div>
          <div class="tasks">
              <div class="inputed-tasks" @dblclick="todo.isCompleted = !todo.isCompleted" v-for="(todo, index) in todos" :key="index" :class="{active: todo.isCompleted}">
                    <div class="tasks-wrapper">
                        <input type="text" name="task-title" id="task-title" :value="todo.title">
                        <input type="text" name="task-description" id="task-description" :value="todo.description">
                    </div>
                    <div class="tasks-button-wrapper">
                        <input type="button" @click="deleteTodo(index)" id="task-button" value="delete">
                    </div>
              </div>
              
          </div>
      </div>
  </div>
</template>

<script>
import AppHeader from './../components/AppHeader.vue'
export default {
    data() {
        return{
            isHidden:true,
            title: null,
            description: null,
            error: null,
            todos: [
                {
                    title: 'drink water',
                    description: 'to stay alive :)',
                    isCompleted: true
                },
                {
                    title: "work hard",
                    description: 'to succeed',
                    isCompleted: false
                },
                {
                    title: "have fun",
                    description: "enjoy ur life",
                    isCompleted: false
                }
            ]
        }
    },
    methods: {
        addNewTask(){
            this.error = null;
            const title = this.title;
            const description = this.description;
            const isCompleted = false;
            if(!title) {
                this.error = 'please add title'
                return ;
            };
            const newTask = {
                title,
                description,
                isCompleted
            };
            this.todos.push(newTask);
            this.isHidden = true;
            this.title = '';
            this.description = '';
        },
        deleteTodo(index) {
            // this.$delete(this.todos, index);
            this.todos.splice(index, 1);  // you can write both 
        },
    },
    components: {
        AppHeader
    }
}
</script>

<style>
.task-wrapper{
    display: flex;
    flex-direction: column;
    position: relative;
    top: 50px;
    align-items: center;
    justify-content: center;
}
.add-task-wrapper{
    display: inline;
    background: rgb(214, 218, 219);
    border: 1px solid transparent;
    border-radius: 5px;
}
.add-task{
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 0 .5rem;
}
.add-task p{
    padding: 1rem;
}
.new-task{
    padding: .4rem;
    color: rgb(214, 218, 219);
    background: black;
    border: 1px solid transparent;
    border-radius: 5px;
}
.new-task:hover{
    transform: scale(.98);
}
.tasks{
    margin-top: 50px;
    display: flex;
    padding: 10px;
    width: 600px;
    background: rgb(214, 218, 219);
    border: 1px solid transparent;
    border-radius: 5px;
    flex-direction: column;
    justify-content: space-between;
}
.tasks-wrapper{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    flex-basis: 33em;
}
.tasks-button-wrapper{
    display: flex;
    align-items: center;
    justify-content: center;
}
#task-title{
    margin: 5px;
    padding: 5px;
    background: black;
    color: rgb(214, 218, 219);
    border: 1px solid transparent;
    border-radius: 5px;
    outline: none;
}
#task-description{
    margin: 5px;
    padding: 5px;
    background: black;
    color: rgb(214, 218, 219);
    border: 1px solid transparent;
    border-radius: 5px;
    outline: none;
}
#task-button{
    padding: 7px;
    color: rgb(214, 218, 219);
    background: black;
    border: 1px solid transparent;
    border-radius: 5px;
}
#task-button:hover{
    transform: scale(.97);
}
.inputed-tasks{
    display: flex;
    justify-content: space-around;
    margin: 10px 0;
    border: 5px solid rgb(110, 103, 103);
    border-radius: 10px;
}
.active{
    border-left: 8px solid green;
}
</style>