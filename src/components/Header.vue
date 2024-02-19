<template>
    <header>
        <h1>{{ title }}</h1>
        <Button text="Add Task" color="green"/>
        <!-- <Button text=" Update Task" color="blue"/>
        <Button text="Delete Task" color="red"/> -->
    </header>
</template>

<script>
    import Button from './Button.vue'

    export default {
        name : 'Header',
        props: {
            title: String,
        },
        // props: ['title'],
        components: {
            Button
        }
    }
</script>

<style scope>
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }
</style>
