<template>
    <header>
        <h1>{{ title }}</h1>
        <Button v-show="homepage" @btn-click="$emit('toggle-add-task')" :text="showAddTask ? 'Close' : 'Add Task'" :color="showAddTask ? 'red' : 'green'"/>
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
            showAddTask: Boolean
        },
        // props: ['title'],
        components: {
            Button
        },
        computed: {
            homepage(){
                if(this.$route.path === '/'){
                    return true;
                }else{
                    return false
                }
            }
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
