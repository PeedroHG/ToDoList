<script lang="ts">
import Input from './Input.vue'
import Button from './Button.vue'
export default {
  data() {
    return {
      novaTask: '',
    }
  },
  components: {
    Input,
    Button,
  },
  methods: {
    adicionarTask() {
      if (this.novaTask.trim()) {
        this.$emit('adicionarTask', this.novaTask)
        this.novaTask = ''
      }
    },
    atualizarInput(valor: string) {
      this.novaTask = valor
    },
  },
}
</script>

<template>
  <section class="topo">
    <img src="@/assets/images/logo.png" class="logo" />
    <Input @input-alterado="atualizarInput"></Input>
    <Button texto="Adicionar" @click="adicionarTask"></Button>
  </section>
</template>

<style scoped>
.topo {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 3rem;
}

.logo {
  width: 2.3rem;
}

@media screen and (min-width: 1000px) {
  .logo {
    width: 3rem;
  }
}
</style>
