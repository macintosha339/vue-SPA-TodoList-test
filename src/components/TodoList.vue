<template>
<div>
    <ul>
        <TodoItem v-for="(todo) in todos" v-bind:index="i" />
    </ul>
</div>
</template>

<script>
import TodoItem from "./TodoItem.vue"
export default {
    props: ['todos'],
    components: {
        TodoItem
    }
}
</script>

<style scoped>
    ul {
        list-style: none;
        margin-top:2.6rem;
        padding: 0;
        margin: 0;
        }
</style>