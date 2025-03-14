<script lang="ts">
import Top from './components/Top.vue'
import ConteudoPrincipal from './components/ConteudoPrincipal.vue'

export default {
  data() {
    return {
      novaTask: '',
    }
  },
  components: {
    Top,
    ConteudoPrincipal,
  },
  methods: {
    adicionarTask(task: string) {
      this.novaTask = task
    },
  },
}
</script>

<template>
  <Top @adicionarTask="adicionarTask"></Top>
  <ConteudoPrincipal :novaTask="novaTask"></ConteudoPrincipal>
</template>


