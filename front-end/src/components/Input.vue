<script lang="ts">
export default {}
</script>

<template>
  <div class="input-container">
    <img src="@/assets/images/pencil-icon.png" class="icon" />
    <input type="text" class="input" placeholder="Digite sua task" />
  </div>
</template>

<style scoped>
.input-container {
  position: relative;
  display: inline-block;
}
input {
  padding: 1rem 1rem 1rem 3rem;
  width: 22rem;
  height: 3.5rem;
  background-color: var(--fundo-input);
  margin: 1.3rem;
  border-radius: 16px;
  line-height: 24px;
  font-size: 16px;
  font-weight: 600;
  color: var(branco-input);
}
.icon {
  position: absolute;
  left: 2.3rem;
  top: 50%;
  transform: translateY(-50%);
  width: 18px;
  height: 18px;
}
</style>
