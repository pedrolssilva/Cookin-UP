<script lang="ts">
import type IReceita from '@/interfaces/IReceita'
import type { PropType } from 'vue'

export default {
  props: {
    receita: { type: Object as PropType<IReceita>, required: true },
  },
}
</script>

<template>
  <article class="receita">
    <header class="receita__cabecalho">
      <img
        :src="`/imagens/receitas/${receita.imagem}`"
        alt=""
        class="receita__imagem"
      />
    </header>
    <section class="receita__corpo">
      <h2 class="paragrafo receita__nome">
        {{ receita.nome }}
      </h2>
    </section>
  </article>
</template>

<style scoped>
.receita {
  display: flex;
  width: 17.625rem;
  max-width: 19.5rem;
  border-radius: 1rem;
  background: var(--branco, #fff);
  box-shadow: 4px 4px 12px 0px rgba(68, 68, 68, 0.05);
  flex-direction: column;
  align-items: center;
}

.receita__corpo {
  padding: 2rem 1rem;
}

.receita__cabecalho {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.5rem;
}

.receita__imagem {
  width: 100%;
  border-radius: 1rem 1rem 0 0;
  display: block;
}

.receita__nome {
  font-weight: 700;
  color: var(--cinza, #444);
}
</style>
