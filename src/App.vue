<template>
  <div id="app">
    <main id="todolist">
      <h1>
        TODO LIST:
      </h1>
      <TodoList v-bind:todos="todos"/>
    </main>
  </div>
</template>

<script>
import TodoList from "./components/TodoList.vue"
export default {
  name: 'app',
  data () {
    return {
      todos: [
        {id: 1, title:"Сделать первый пункт ", completed: false},
        {id: 2, title:"Создать свой телеграм", completed: false},
        {id: 3, title:"Выспаться", completed: false}
      ]
    }
  },
  components: {
    TodoList
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
* {
	margin:0;
	padding:0;
	box-sizing:border-box;
}
html, body {
	background:#7CB6FC;
	font-size:1.1rem;
	font-family:'Helvetica', sans-serif;
	height:100%;
}
#todolist {
	margin:4rem auto;
	padding:2rem 3rem 3rem;
	max-width:500px;
	background:#617FA0;
	color:#FFF;
  border-radius: 10px;
	-webkit-box-shadow: 10px 10px 50px 0px rgba(0,0,0,0.75);
  -moz-box-shadow: 10px 10px 50px 0px rgba(0,0,0,0.75);
  box-shadow: 10px 10px 50px 0px rgba(0,0,0,0.75);
}
#todolist h1 {
    font-weight:normal;
    font-size:2.6rem;
    letter-spacing:0.05em;
    border-bottom:1px solid rgba(255,255,255,.3); 
    margin-bottom: 1em;
}
</style>


