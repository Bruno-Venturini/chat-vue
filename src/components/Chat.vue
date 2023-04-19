<template>
  <div class="container">
    <div class="header">
      Atendimento Online
    </div>
    <div class="messages">
      <Message v-for="(msg, index) in mensagens" :key="index" :isUser="msg.isUser" :mensagem="msg.mensagem"></Message>
    </div>
    <div class="footer">
      <input id="inputMensagem" class="chat-input" placeholder="Digite sua mensagem..." type="text" v-model="conteudoMensagem" @keyup.enter="enviarMensagem">
      <button id="botao" @click="enviarMensagem" class="submit-button">ENVIAR</button>
    </div>
  </div>
</template>

<script setup>
import Message from "./Message";
import { ref } from 'vue';

const mensagens = ref([{
  mensagem: "Olá",
  isUser: false
}]);

let conteudoMensagem = '';

function appendMessagem(mensagem, isUser) {
  mensagens.value.push({
    mensagem: mensagem,
    isUser: isUser
  })
}

async function enviarMensagem(){
  const mensagem = conteudoMensagem.trim();
  if (mensagem !== '') {
    appendMessagem(mensagem, true);
    conteudoMensagem = '';
  }
}
</script>

<style scoped>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.container {
  font-family: 'Roboto', sans-serif;
  border: 1px solid #ccc;
  border-radius: 8px;
  width: 400px;
  margin: 50px auto;
  display: flex;
  flex-direction: column;
}

.header {
  font-size: 24px;
  font-weight: bold;
  color: #333;
  padding: 16px;
  background-color: #fff;
  border-bottom: 1px solid #ccc;
}

.messages {
  display: flex;
  flex-direction: column;
  overflow-y: auto;
  padding: 16px;
  background-color: #f7f7f7;
  flex-grow: 1;
}

.chat-input {
  width: 100%;
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 8px;
  font-size: 16px;
  margin-right: 8px;
}

.submit-button {
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 8px;
  padding: 12px;
  font-size: 16px;
  font-weight: bold;
  cursor: pointer;
}

.submit-button:hover {
  background-color: #3e8e41;
}

.footer {
  display: flex;
  align-items: center;
  padding: 16px;
  background-color: #f7f7f7;
  border-top: 1px solid #ccc;
}
</style>