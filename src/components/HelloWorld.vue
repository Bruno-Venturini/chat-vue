<template>
  <div>
  <body>
    <header class="div-header">
      Atendimento online
    </header>
    <div class="div-body">
      <form id="idForm">
        <div class="campos-esquerda">
          <label for="input1">Atendente diz:</label>
          <input id="input1" type="text" placeholder="Blabla blabla blabla">

          <label for="input1">Atendente diz:</label>
          <input id="input1" type="text" placeholder="Blabla blabla blabla">
        </div>
        <div id="campos-direita" class="campos-direita">
          <label for="input1">Você diz:</label>
          <input id="input1" type="text" placeholder="Blabla blabla blabla">

          <label for="input1">Você diz:</label>
          <input id="input1" type="text" placeholder="Blabla blabla blabla">
        </div>
      </form>
    </div>
    <footer class="div-footer">
      <div class="botoes-footer">
        <input id='inputMensagem' class="chat" placeholder="Digite sua mensagem..." type="text"> <button id='botao'class="submit">ENVIAR</button>
      </div>
    </footer>
  </body>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
input {
  border-style: ridge;
}

body{
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  font-size: small;
  border: 2px;
  border-style: ridge;
  display: flex;
  flex-direction: column;
  width: 400px;
  height: auto;
  margin-left: 125px;
}

.div-header{
  font-family: "Comic Sans MS";
  font-weight: bolder;
  display: inherit;
  flex-direction: inherit;
  color: purple;
  padding: 2px;
  border: 1px;
  border-style: solid;
}

.div-body {
  border: 2px;
  border-style: solid;
  height: auto;
  margin-left: 5px;
  margin-right: 5px;
  margin-top: 5px;
}

.campos-esquerda{
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  margin-left: 10px;
  margin-top: 5px;
}

.campos-esquerda input{
  margin-bottom: 4px;
}

.campos-direita{
  margin-right: 10px;
  display: flex;
  flex-direction: column;
  align-items: flex-end;

}
.campos-direita input{
  margin-bottom: 4px;
}


.div-footer {
  margin-bottom: 20px;
  display: inherit;
  flex-direction: row;
}

.botoes-footer {
  display: inherit;
  flex-direction: inherit;
  margin-top: 20px;
  align-items: center;
  margin-left: 4px;
  margin-right: 4px;
  width: 100%;
}
.div-body input::placeholder {
  color: black;
}

.chat {
  align-self: start;
  width: 75%;
}

.submit{
  margin-left: 5px;
  align-self: center;
  text-align: center;
  width: 25%;
  color: green;
  font-weight: bold;
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}

</style>
