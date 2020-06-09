<template>
    <div id="tarefa">
        <div class="tarefas" v-for="(tarefa, index) in tarefas" :key="index">
            {{ tarefa.descricao }}
        </div>
    </div>
</template>

<script>
export default {
    name: "tarefa",
    props: ['tarefas']
}
</script>

<style>
  #tarefa{
        width: 300px;
        height: 200px;
        border: black 2px solid;
        margin: 30px auto 50px auto;
        background-color: white;
        flex-wrap: wrap;
        overflow: auto;
    }
    .tarefas{
        width: tarefa;
        margin-left: 20px;
        height: 20px;
        border-radius: 2px;
        border: 1px black solid;
        margin: 1px 1px 1px 1px;
    }
</style>