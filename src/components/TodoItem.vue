<template>
    <li>
        <span>
            <input type="checkbox">
            {{ todo.title}}
        </span>
    </li>
</template>

<script>
export default {
    props: {
        todo: {
            type: Object,
            required: true
        },
        index: Number
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
</style>