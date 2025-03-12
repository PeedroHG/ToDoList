<script lang="ts">
export default {
  props: {
    texto: {
      type: String,
      required: true,
    },
  },
}
</script>

<template>
  <button class="botao-add">{{ texto }}</button>
</template>

<style scoped>
.botao-add {
    padding: 1rem;
    width: 17rem;
    height: 3.2rem;
    line-height: 24px;
    font-size: 16px;
    font-weight: 600;
    border-radius: 16px;
    color: var(--branco-tiulo);
    background-color: var(--azul);
}
</style>
