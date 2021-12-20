<template>
    <div>
        <h3>Todos</h3>
        <div class="todos">
            <div v-for="(todo, index) in allTodos" :key="index" class="todo">
                {{  todo.title }}
            </div>
        </div>
    </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
    name: "Todos",
    computed: mapGetters(['allTodos'])
}

</script>


<style>


</style>