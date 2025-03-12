<script lang="ts">
export default {
  props: {
    task: {
      type: String,
      required: true,
    },
  },
}
</script>

<template>
  <li class="item-lista">
    <input type="checkbox" class="checkbox" />
    <p class="text">{{ task }}</p>
  </li>
</template>

<style scoped>
.item-lista {
  padding-bottom: 0.9rem;
  display: flex;
  align-items: center;
}
.text {
  margin-left: 0.7rem;
}
.checkbox {
  appearance: none;
  background-color: var(--fundo-input);
  border-radius: 0.25rem;
  width: 1.25rem;
  height: 1.25rem;
  display: inline-block;
  position: relative;
}
</style>
