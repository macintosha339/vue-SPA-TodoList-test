<template>
    <li>
        <span v-bind:class="{done: todo.completed}">
            <input type="checkbox" v-on:change="todo.completed = !todo.completed">
            {{ todo.title}}
        </span>
        <button class="btn_delete" @click="openModal">Удалить</button>
        <Modal v-model="modalOpen"/>
    </li>
</template>

<script>
import Modal from './Modal'
export default {
    props: {
        todo: {
            type: Object,
            required: true
        },
        index: Number
    },
    components: {
        Modal
    },
    data() {
        return {
            modalOpen: false
        }
    },
    methods: {
        openModal() {
            this.modalOpen= !this.modalOpen;
        }
    }
}
</script>

<style scoped>
    li {
    transition: transform 1s;
    display: flex;
	margin: 0px -3rem 18px;
	padding: 0.5rem 3rem;
	justify-content: space-between;
	align-items: center;
    color: #838383;
    background-color: #FFFFFF;
    -webkit-box-shadow: 0px 11px 33px -9px rgba(0,0,0,0.75);
    -moz-box-shadow: 0px 11px 33px -9px rgba(0,0,0,0.75);
    box-shadow: 0px 11px 33px -9px rgba(0,0,0,0.75);
    }
    input{
      margin-right:1.5em;
    }
    .done{
        opacity: .6;
        text-decoration: line-through;
    }
   .btn_delete {
  
  
  display: inline-block;
  padding: 5px 10px;
  margin: 5px 10px;
  border: 0;
  border-radius: 5px;
  box-shadow: 0 0 20px 20px #f13737 inset, 0 0 0 0 #f13737;
  letter-spacing: 2px;
  color: white;
  transition: .15s ease-in-out;
}
.btn_delete:hover {
  box-shadow: 0 0 10px 0 #f13737 inset, 0 0 10px 4px #f13737;
  color: #f13737;
}
</style>