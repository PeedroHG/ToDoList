<script lang="ts">
import Input from './Input.vue'
export default {
  components: {
    Input,
  },
}
</script>

<template>
  <section class="topo">
    <img src="@/assets/images/logo.png" class="logo" />
    <Input></Input>
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
