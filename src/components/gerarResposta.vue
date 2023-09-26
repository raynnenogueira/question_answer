<template>
  <div>
    <label for="question">Faça uma pergunta:</label>
    <input v-model="pergunta" type="text">
    <button @click="gerarResposta">Gerar Resposta</button>
    <button @click="limpar">Limpar</button>
    <p v-if="answer" class="cor-resposta">{{ answer }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      pergunta: "",
      answer: "",
    };
  },
  
  methods: {
    gerarResposta() {
      if (this.pergunta === "") {
        return; // Não gerar resposta se a pergunta estiver vazia
      }

      const answer = [ // arrays
        'Com certeza',
        'É... não tenho certeza!',
        'Claro que não',
        'Acho difícil',
        'Possivelmente não'
      ];

      const indiceAleatorio = Math.floor(Math.random() *         answer.length); // Gerar um índice aleatório

      this.answer = answer[indiceAleatorio]; // Definir a resposta com base no índice aleatório
    },
    
    limpar() { // aqui vai limpar a pergunta e a resposta
      this.pergunta = "";
      this.answer = "";
    },
  },
};
</script>

<style scoped>
  .cor-resposta {
    color: green; 
  }
  
  label {
    font-weight: bold;
    font-size: 20px;
    color: #918A94;
  }
  
  input {
    width: 100%;
    padding: 5px;
    margin-bottom: 10px;
  }
  
  button {
    border-radius: 5px;
    padding: 5px 10px;
    background-color: #38174D;
    color: #fff;
    border: none;
    cursor: pointer;
    margin-right: 10px;
  }

  button:hover {
    background-color: #5E0099;
  }
</style>
