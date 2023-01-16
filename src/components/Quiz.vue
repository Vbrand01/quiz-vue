<script>
export default{
    name: 'Quiz',
}

import { ref, computed } from 'vue'

const questions = ref([
  {
    question: 'De quem é a famosa frase “Penso, logo existo”?',
    answer: 2,
    options: [
      'Sócrates',
      'Platão',
      'Descartes',
      'Francis Bacon',
      'Galileu Galilei'
    ],
    selected: null
  },
  {
    question: 'De onde é a invenção do chuveiro elétrico?',
    answer: 3,
    options: [
      'Itália',
      'França',
      'Inglaterra',
      'Brasil',
      'Austrália'
    ],
    selected: null
  },
  {
    question: 'Qual o livro mais vendido no mundo a seguir à Bíblia?',
    answer: 0,
    options: [
      'Dom Quixote',
      'O Pequeno Príncipe',
      'O Senhor dos Anéis',
      'Ela, a Feiticeira',
      'Um Conto de Duas Cidades'
    ],
    selected: null
  },
  {
    question: 'Quantas casas decimais tem o número pi?',
    answer: 3,
    options: [
      'Duas',
      'Milhares',
      'Vinte',
      'Infinitas',
      'Centenas'
    ],
    selected: null
  },
  {
    question: 'Qual o número mínimo de jogadores em cada time numa partida de futebol?',
    answer: 1,
    options: [
      '8',
      '7',
      '9',
      '5',
      '10'
    ],
    selected: null
  },
  {
    question: 'Quanto tempo a luz do Sol demora para chegar à Terra?',
    answer: 2,
    options: [
      '12 minutos',
      '12 horas',
      '8 minutos',
      '1 dia',
      '12 segundos'
    ],
    selected: null
  },
  {
    question: 'Qual personagem folclórico costuma ser agradado pelos caçadores com a oferta de fumo?',
    answer: 4,
    options: [
      'Lobisomem',
      'Negrinho do Pastoreio',
      'Boitatá',
      'Saci',
      'Caipora'
    ],
    selected: null
  },
  {
    question: 'Qual a montanha mais alta do Brasil?',
    answer: 0,
    options: [
      'Pico da Neblina',
      'Monte Roraima',
      'Pico da Bandeira',
      'Pico da Bandeira',
      'Pico Paraná'
    ],
    selected: null
  },
  {
    question: 'Como é a conjugação do verbo caber na 1.ª pessoa do singular do presente do indicativo?',
    answer: 2,
    options: [
      'Que eu caiba',
      'Ele cabe',
      'Eu caibo',
      'Eu cabo',
      'Nenhuma das alternativas'
    ],
    selected: null
  },

  {
    question: 'Qual destes países é transcontinental?',
    answer: 1,
    options: [
      'Filipinas',
      'Rússia',
      'Marrocos',
      'Groenlândia',
      'Tanzânia'

    ],
    selected: null
  },

  {
    question: 'Em qual das orações abaixo a palavra foi empregada incorretamente?',
    answer: 4,
    options: [
      'É um mau vendedor.',
      'Mais uma vez, portou-se mal.',
      'Mal falou nele, o fulano apareceu.',
      'Esse é o mal de todos.',
      'É um homem mal.'

    ],
    selected: null
  },

  {
    question: 'Qual foi o recurso utilizado inicialmente pelo homem para explicar a origem das coisas?',
    answer: 3,
    options: [
      'A Matemática',
      'A Filosofia',
      'A Biologia',
      'A Mitologia',
      'A Astronomia'

    ],
    selected: null
  },

  {
    question: 'Qual o maior animal terrestre?',
    answer: 0,
    options: [
      'Elefante africano',
      'Girafa',
      'Baleia Azul',
      'Tubarão Branco',
      'Dinossauro'

    ],
    selected: null
  },

  {
    question: 'Qual o tema do famoso discurso Eu Tenho um Sonho, de Martin Luther King?',
    answer: 1,
    options: [
      'Intolerância religiosa',
      'Igualdade das raças',
      'Justiça para os menos favorecidos',
      'Prêmio Nobel da Paz',
      'Luta contra o Apartheid'

    ],
    selected: null
  },

  {
    question: 'Quais os nomes dos três Reis Magos?',
    answer: 2,
    options: [
      'Melchior, Noé e Galileu',
      'Gaspar, Nicolau e Natanael',
      'Belchior, Gaspar e Baltazar',
      'Belchior, Gaspar e Nataniel',
      'Gabriel, Benjamim e Melchior'

    ],
    selected: null
  },

  {
    question: 'Quais são os cromossomos que determinam o sexo masculino?',
    answer: 3,
    options: [
      'Os V',
      'Os X',
      'Os Z',
      'Os Y',
      'Os W'

    ],
    selected: null
  },

  {
    question: 'Como se chamam os vasos que transportam sangue do coração para a periferia do corpo?',
    answer: 0,
    options: [
      'artérias',
      'ventrículos',
      'átrios',
      'veias',
      'aurículos'

    ],
    selected: null
  },

  {
    question: 'Em que oceano fica Madagascar?',
    answer: 0,
    options: [
      'Oceano Ártico',
      'Oceano Antártico',
      'Oceano Atlântico',
      'Oceano Pacífico',
      'Oceano Índico'

    ],
    selected: null
  },

  {
    question: 'Qual o metal cujo símbolo químico é o Au?',
    answer: 1,
    options: [
      'Prata',
      'Ouro',
      'Cobre',
      'Mercúrio'
    ],
    selected: null
  },

  {
    question: 'Quem viveu, segundo a Bíblia, 969 anos?',
    answer: 3,
    options: [
      'Jesus Cristo',
      'Benjamim',
      'Noé',
      'Matusalém',
      'Abel'
    ],
    selected: null
  },

  {
    question: 'Quem pintou o teto da capela sistina?',
    answer: 0,
    options: [
      'Michelangelo',
      'Leonardo da Vinci',
      'Donatello',
      'Sandro Botticelli'
    ],
    selected: null
  },

  {
    question: 'O que é Pix?',
    answer: 2,
    options: [
      'Conjunto de formas de pagamento realizados por subadquirentes',
      'Plano de investimento de baixo risco do Banco do Brasil',
      'Meio de pagamento instantâneo criado pelo Banco Central do Brasil',
      'Forma de pagamento online',
      'Produtos de investimento financeiro criados pelo Banco Central do Brasil'

    ],
    selected: null
  },

  {
    question: 'Quantos fusos horários existem na Rússia?',
    answer: 0,
    options: [
      '11',
      '9',
      '10'
    ],
    selected: null
  },
  {
    question: 'Qual é a flor nacional do Japão?',
    answer: 1,
    options: [
      'Flor de Rosa',
      'Flor de Cerejeira',
      'Flor Japonesa'
    ],
    selected: null
  },
  {
    question: 'Quem é conhecido como rei do futebol?',
    answer: 2,
    options: [
      'CR7',
      'Messi',
      'Pelé'
    ],
    selected: null
  }
])


const quizCompleted = ref(false)
const currentQuestion = ref(0)
const score = computed(() => {
  let value = 0
  questions.value.map(q => {
    if (q.selected == q.answer){
      value++
    }
  })
  return value
})

const getCurrentQuestion = computed(()=> {
  let question = questions.value[currentQuestion.value]
  question.index = currentQuestion.value
  return question
})

const SetAnswer = evt => {
  questions.value[currentQuestion.value].selected = evt.target.value
  evt.target.value = null
}

const NextQuestion = () => {
  if (currentQuestion.value < questions.value.length -1){
    currentQuestion.value++
  }else{
    quizCompleted.value = true
  }
}

</script>

<template>
<div>
  <main class="app">
    <h1>Quiz</h1>

    <section class="quiz" v-if="!quizCompleted">
      <div class="quiz-info">
        <span class="question">{{ getCurrentQuestion.question }}</span>
        <!-- <span class="score">{{  score }} / {{ questions.length }}</span> -->
      </div>

      <div class="options">
        <label 
        v-for="(option, index) in getCurrentQuestion.options"
        :key="index"
        :class="`option ${
          getCurrentQuestion.selected == index
          ? index == getCurrentQuestion.answer
          ? 'correct'
          : 'wrong'
          : ''
        } ${
          getCurrentQuestion.selected != null &&
          index != getCurrentQuestion.selected
          ? 'disabled'
          : ''
        }`">

          <input 
          type="radio" 
          :name="getCurrentQuestion.index"
          :value="index"
          v-model="getCurrentQuestion.selected"
          :disabled="getCurrentQuestion.selected"
          @change="SetAnswer">

          <span>{{ option }}</span>
        </label>
      </div>

      <button 
      @click="NextQuestion"
      :disabled="!getCurrentQuestion.selected"
      >

      {{ 
          getCurrentQuestion.index == questions.length -1
          ? 'Finish'
          : getCurrentQuestion.selected == null
            ? 'Select an option'
            : 'Next Question'
      }}
    
    </button>
    </section>

    <section v-else>
      <h2>Você terminou o teste!</h2>
      <p>Você acertou: {{ score }} / {{ questions.length }}</p>
    </section>
  </main>
</div>
</template>


<style>

.app{
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 2rem;
  min-height: 100vh;
}

h1{
  font-size: 2rem;
  margin-bottom: 2rem;
}

.quiz{
  background-color: rgb(27, 27, 27);
  padding: 2rem;
  width: 100%;
  max-width: 640px;
  border-radius: 10px;
}

.quiz-info {
  display: flex;
  justify-content: space-between;
  margin-bottom: 1rem;
}

.quiz-info .question {
  color: #d6d6d6;
  font-size: 1rem;
  font-weight: 600;
}

.options{
  margin-bottom: 1rem;
}

.option{
  display: block;
  padding: 1rem;
  background-color: #555555;
  border-radius: 0.5rem;
  margin-bottom: 0.5rem;
  cursor: pointer;
}

.option:hover{
  background-color: #757575;
}

.option.correct {
  background-color: rgb(0, 255, 149);
  color: black;
}

.option.wrong {
  background-color: rgb(255, 0, 64);
}

.option:last-of-type{
  margin-bottom: 0;
}

.option.disabled {
  opacity: 0.5s;
}

.option input {
  display: none;
}

button {
  appearance: none;
  outline: none;
  border: none;
  cursor: pointer;
  padding: 0.5rem 1rem;
  background-color: rgb(89, 0, 255);
  color: #dfdfdf;
  font-weight: 700;
  text-transform: uppercase;
  font-size: 1rem;
  width: 100%;
  border-radius: 0.5rem;
}

button::disabled {
  opacity: 0.5;
}

h2{
  font-size: 2rem;
  margin-bottom: 2rem;
  text-align: center;
}

p{
  color: #dadada;
  text-align: center;
}

.score{
  font-size: 13px;
}

</style>
