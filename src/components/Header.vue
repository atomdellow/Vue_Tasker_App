/* eslint-disable */
<template>
    <header>
        <h1>{{ title }}</h1>
        <NewBtn 
            @btn-click="$emit('toggle-add-task')" :text="showAddTask ? 'Close':'Add Task'" 
            :color="showAddTask ? 'red' : 'green'" 
        />
    </header>
 
</template>

<script>
import NewBtn from './NewBtn.vue';

    export default{
    name: "HeaderComp",
    props: {
        title: {
            title: String,
        showAddTask: Boolean
        },
        components: {
            NewBtn,
        },
    },
    components: { NewBtn },
}
</script>

<style scoped>
    Header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }
</style>