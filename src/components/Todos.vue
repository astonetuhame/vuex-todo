<template>
    <div>
        <h3>Todos</h3>
        <div class="todos">
            <div v-for="(todo, index) in allTodos" :key="index" class="todo">
                {{  todo.title }}
                <i @click="deleteTodo(todo.id)" class="fas fa-trash-alt"></i>
            </div>
        </div>
    </div>
</template>

<script>
import { mapGetters, mapActions } from 'vuex'

export default {
    name: "Todos",
    methods:{
        ...mapActions(['fetchTodos', "deleteTodo"])
    },
    computed: mapGetters(['allTodos']),
    created(){
        this.fetchTodos()
    }
}

</script>


<style scoped>
    .todos {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        
    }

    .todo{
        border: 1px solid #ccc;
        background: #41b883;
        padding: 1rem;
        border-radius: 5px;
        text-align: center;
        position: relative;
        cursor: pointer
    }

    i {
        position: absolute;
        bottom: 10px;
        right: 10px;
        color: #fff;
        cursor: pointer
    }

</style>