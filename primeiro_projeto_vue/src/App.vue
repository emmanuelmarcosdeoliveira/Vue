<script setup>
const bemVindo = "Hello World";
const meuObj = {
  nome: "Emmanuel",
  idade: 45,
  profissao: "develper Front-end",
};
function dizOla(nome) {
  return `${nome} Seja bem vindo`;
}
const botaoHabilitado = false;

const imagemPraia =
  "https://static.vecteezy.com/ti/fotos-gratis/t2/2073926-fundo-de-praia-tropical-e-ceu-azul-gratis-foto.jpg";

const imageSuperMan =
  "https://www.otempo.com.br/image/contentid/policy:1.2888315:1686762481/image-Uma-versao-do-Superman-e-poderosa-demais-para-aparecer-nos-cinemas.jpg?f=3x2&w=1224";
const gostaDePraia = false;
const gostaSuperMan = false;
</script>

<template>
  <h1>{{ dizOla("Emmanuel") }}</h1>
  <img v-if="gostaDePraia" :src="imagemPraia" alt="" />
  <img v-else-if="gostaSuperMan" :src="imageSuperMan" alt="" />
  <strong v-else>Não goosta de nenhuma imagem</strong>
  <button :disabled="botaoHabilitado">Botão</button>
</template>
<style scoped>
img {
  max-width: 400px;
}
</style>
