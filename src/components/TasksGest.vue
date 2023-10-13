<template>
    <div :key="task.id" v-for="task in tasks">
        <SingleTaskGest @toggle-reminder="$emit('toggle-reminder', task.id)" 
        @delete-task="$emit('delete-task', task.id)" :task="task"></SingleTaskGest>
    </div>
</template>

<script>

import SingleTaskGest from './SingleTaskGest'

export default {
    name: 'TasksGest',
    props: {
        tasks: Array,
    },
    components: {
        SingleTaskGest,
    },
    emits: ['delete-tasks','toggle-reminder'],
}
</script>