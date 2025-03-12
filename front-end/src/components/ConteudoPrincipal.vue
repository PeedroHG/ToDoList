<script lang="ts">
import ItemLista from './ItemLista.vue'
import Linha from './Linha.vue';

export default {
  data() {
    return {
      tasks: ['Ir a academia', 'Estudar para geometria analítica', 'Comprar abacate', 'Jogar bola sábado de manhã'] as string[],
    }
  },
  components: {
    ItemLista,
    Linha
  },
}
</script>

<template>
  <section class="tasks">
    <ul>
      <ItemLista v-for="task in tasks" :task="task" :key="task"></ItemLista>
    </ul>
  </section>
  <Linha cor="amarelo"></Linha>
</template>

<style scoped>
.tasks {
  margin-top: 4rem;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding-left: 3rem;
}
</style>
