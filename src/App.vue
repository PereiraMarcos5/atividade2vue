<template>
  <div id="app">
    <caixa @criar="adicionarTarefa($event)"/>
    <tarefa :tarefas="tarefas" />
  </div>
</template>

<script>
import caixa from "./components/caixa.vue"
import tarefa from "./components/tarefas.vue"
export default {
  name: 'App',
  components: {
    caixa,
    tarefa
  },
  data: function() {
    return {
      tarefas: []
    };
  },
  methods: {
    adicionarTarefa: function(event) {
      this.tarefas.push({descricao: event.texto});
    }
  }
};
</script>

<style>
</style>