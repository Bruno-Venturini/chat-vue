<template>
  <div v-bind:class="[isUser ? 'mensagem-direita' : 'mensagem-esquerda']">
    <label>{{ isUser ? 'Você' : 'Bot' }}</label>
    <p>{{ mensagem }}</p>
  </div>
</template>

<script>
export default {
  name: 'Message',
  props: {
    mensagem: String,
    isUser: Boolean,
  },
};
</script>

<style scoped>
.mensagem-esquerda {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  margin-bottom: 10px;
}

.mensagem-direita {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  margin-bottom: 10px;
}

.mensagem-esquerda label {
  font-weight: bold;
  margin-right: 5px;
  color: #4c4c4c;
}

.mensagem-direita label {
  font-weight: bold;
  margin-left: 5px;
  color: #4c4c4c;
}

.mensagem-esquerda p {
  background-color: #fff;
  padding: 5px;
  border-radius: 10px;
  box-shadow: 1px 1px 2px #d9d9d9;
}

.mensagem-direita p {
  background-color: #87CEEB;
  color: #fff;
  padding: 5px;
  border-radius: 10px;
  box-shadow: 1px 1px 2px #d9d9d9;
}
</style>