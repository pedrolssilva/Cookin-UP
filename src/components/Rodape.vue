<script lang="ts">
export default {}
</script>

<template>
  <footer class="rodape">
    <p>
      Desenvolvido por Alura | {{ new Date().getFullYear() }} - Projeto fictício
      sem fins comerciais
    </p>
  </footer>
</template>

<style scoped>
.rodape {
  background: var(--verde-escuro, #263a29);
  padding: 1.5rem 7.5rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

@media only screen and (max-width: 1300px) {
  .rodape {
    padding: 1.5rem 3.75rem;
  }
}

@media only screen and (max-width: 767px) {
  .rodape {
    padding: 1.5rem;
  }
}
</style>
