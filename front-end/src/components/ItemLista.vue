<script lang="ts">
export default {
  props: {
    task: {
      type: String,
      required: true,
    },
    selecionado: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    marcarTask() {
      this.$emit('atualizar-selecionado', this.task, !this.selecionado);
    },
  },
}
</script>

<template>
  <li class="item-lista">
    <input
      type="checkbox"
      :class="['checkbox', { selecionado: selecionado }]"
      :checked="selecionado"
      @click="marcarTask"
    />
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
  cursor: pointer;
}

.checkbox.selecionado {
  background-image: url('@/assets/images/checkmark.png');
  background-size: 60%;
  background-position: center;
  background-repeat: no-repeat;
}
</style>
