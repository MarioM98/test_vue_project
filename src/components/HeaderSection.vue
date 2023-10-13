<template>
    <header>
        <h1>{{ title }}</h1>
        <ButtonSection @btn-click="$emit('toggle-add-task')" 
        :text="showAddTask ? 'Close' : 'Add Task'" 
        :color="showAddTask ? 'red' : 'green'"/>
    </header>
</template>

<script>

import ButtonSection from './ButtonSection.vue';

export default {
    name: 'HeaderSection',
    props: {
        title: String,
        showAddTask: Boolean
    },
    components: {
        ButtonSection
    }
}
</script>

<style scoped>
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }
</style>