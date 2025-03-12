<script lang="ts">
import Input from './Input.vue'
import Button from './Button.vue'
export default {
  components: {
    Input,
    Button
  },
}
</script>

<template>
  <section class="topo">
    <img src="@/assets/images/logo.png" class="logo" />
    <Input></Input>
    <Button texto="Adicionar"></Button>
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
</style>
