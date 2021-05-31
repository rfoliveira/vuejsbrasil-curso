<template>
    <div>
        <h1>Minha lista de tarefas</h1>
        <button @click="() => showList = !showList">Ver a lista</button>
        <br>
        <ul v-if="showList">
            <!-- sem iteração -->
            <!-- <li>{{ tasks[0].name }}</li>-->
            <li v-for="(task, index) in tasks" :key="`${task}-${index}`">
                {{ task.name }}
            </li>
        </ul>
        <!-- esse bind funciona por estar logo após um v-if -->
        <p v-else>A lista tá escondida</p>
    </div>
</template>

<script>
export default {
    data: () => ({
        tasks: [
            { 
                name: 'Fazer o curso',
                isDone: false
            },
            { 
                name: 'Fazer outra coisa',
                isDone: true
            }
        ],
        showList: false
    })
}
</script>