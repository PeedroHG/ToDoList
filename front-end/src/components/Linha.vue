<script lang="ts">
import { defineComponent, type PropType } from 'vue'

type Cor = 'azul' | 'amarelo'

export default defineComponent({
  props: {
    cor: {
      type: String as PropType<Cor>,
      required: true,
    },
  },
})
</script>

<template>
  <hr :class="['linha', cor]" />
</template>

<style scoped>
.linha {
  border: 0;
  margin: 0.5rem 4rem;
}

.azul {
  border-top: 2px solid var(--azul); /* Estilo para a cor azul */
}

.amarelo {
  border-top: 2px solid var(--amarelo-linha); /* Estilo para a cor laranja */
}
</style>
