<script lang="ts">
import ItemLista from './ItemLista.vue'
import Linha from './Linha.vue'

export default {
  data() {
    return {
      tasks: [
        'Ir a academia',
        'Estudar para geometria analítica',
        'Comprar abacate',
        'Jogar bola sábado de manhã',
      ] as string[],
      tasksFeitas: [] as string[],
    }
  },
  components: {
    ItemLista,
    Linha,
  },
  methods: {
    atualizarSelecionado(task: string, novoEstado: boolean) {
      if (novoEstado) {
        this.tasks = this.tasks.filter((t) => t !== task) 
        this.tasksFeitas.push(task) 
      } else {
        this.tasksFeitas = this.tasksFeitas.filter((t) => t !== task) 
        this.tasks.push(task)
      }
    },
  },
}
</script>

<template>
  <div class="tasks a-fazer">
    <ul>
      <ItemLista
        v-for="(task, index) in tasks"
        :task="task"
        :key="index"
        :selecionado="false"
        @atualizar-selecionado="atualizarSelecionado"
      ></ItemLista>
    </ul>
  </div>
  <Linha cor="azul" v-if="tasks.length != 0"></Linha>
  <div class="tasks feitas">
    <ul>
      <ItemLista
        v-for="(task, index) in tasksFeitas"
        :task="task"
        :key="index"
        :selecionado="true"
        @atualizar-selecionado="atualizarSelecionado"
      ></ItemLista>
    </ul>
  </div>

  <Linha cor="amarelo" v-if="tasksFeitas.length != 0"></Linha>
</template>

<style scoped>
.tasks {
  margin-top: 4rem;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding-left: 3rem;
}
.feitas {
  margin-top: 1.5rem;
}
</style>
