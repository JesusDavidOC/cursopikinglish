<template>
  <div>
    <div class="row">
      <h3 id="subTitulo">COMMON ORDERS</h3>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <p class="parrafo">
        Usa las siguientes órdenes en la vida cotidiana, compártelas con alguien
        más
      </p>
    </div>
    <div class="row" v-for="item in palabrasP83">
      <div class="col-sm-1"></div>
      <h4 class="parrafo">{{ item }}</h4>
    </div>

    <div class="row">
      <h3 id="subTitulo">PALABRAS PARA PEDIR INFORMACIÓN CON HOW</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
      <listaIndex :tabla="$data.tablaP84" />
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">PRACTICE</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" id="text">
        <p class="fa fa-diamond fuenteDiamon" ></p>
        <a id="textPractice"
          >Ubica la forma correspondiente del verbo en las siguientes
          oraciones.</a
        >
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div class="col-sm-12">
          <tablaTC :cuestionario="tablaP84P2" />
        </div>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">READING COMPREHENSION</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h3 style="text-align: justify">{{ comprension85 }}</h3>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">QUESTIONS</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6" id="text">
        <opcionMultiple
          :options="$data.cuestionarioP85"
          :rEsperadas="$data.respuestasCuestionarioP85"
          @respuestas="$data.mensajeRespuestasP85 = $event"
        />
      </div>
      <b-modal ref="my-modalP85" hide-footer title="RESULTADO">{{
        mensajeRespuestasP85
      }}</b-modal>
      <div class="col-sm-1"></div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-3">
        <b-button variant="primary" @click="showModal('my-modalP85')"
          >VERIFICAR PREGUNTAS</b-button
        >
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">OTRAS PREGUNTAS DE INFORMACIÓN</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div
        class="col-sm-12 row"
        style="margin-bottom: 3em"
        v-for="(object, index) in otrasPreguntasInfoP86"
      >
        <div class="col-sm-2" id="numeroMagico2">{{ object.palabra }}</div>
        <div class="col-sm-2">
          <h3 style="margin-top: 0.4em">{{ object.description }}</h3>
        </div>
        <div class="col-sm-2" v-for="item in object.items">
          <h3 style="margin-top: 0.4em">{{ item }}</h3>
        </div>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">PREGUNTAS DE INFORMACION PARA CONOCER A ALGUIEN</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div class="col-sm-12" style="text-align: left">
          <tablaTC :cuestionario="tablaP86" />
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import posiblesRespuestasTabla from "./posiblesRespuestasTabla";
import opcionMultiple from "./opcionMultiple";
import listaIndex from "./listaIndex";
import inputChecked from "./inputChecked";
import tablaTC from "./tablaTraduccionCodigos";
export default {
  methods: {
    showModal(text) {
      this.$refs[text].show();
    },
  },
  components: {
    listaIndex,
    inputChecked,
    tablaTC,
    opcionMultiple,
  },
  data() {
    return {
      tablaP86: {
        fields: [
          { key: "english", label: "English" },
          { key: "spanish", label: "Spanish" },
        ],
        items: [
          {
            english: "What is your name?",
            spanish: "¿Cuál es tu nombre?",
          },
          {
            english: "How old are you",
            spanish: "¿Cuántos años tienes?",
          },
          {
            english: "When is your birthday?",
            spanish: "¿Cuándo es tu cumpleaños?",
          },
          {
            english: "Where do you live?",
            spanish: "¿Dónde vives?",
          },
          {
            english: "Who do you live with?",
            spanish: "¿Con quién vives?",
          },
          {
            english: "When were you born?",
            spanish: "¿Dónde naciste?",
          },
          {
            english: "Which countries have you been to?",
            spanish: "¿En cuáles países has estado?",
          },
          {
            english: "What do you do for a living?",
            spanish: "¿Qué haces para ganarte la vida?",
          },
        ],
      },
      otrasPreguntasInfoP86: [
        {
          palabra: "WHAT",
          description: "QUÉ, CUÁL O LO QUE.",
          items: [
            "-What is this? ¿Qué es esto?",
            "-What is your name? ¿Cuál es tu nombre?",
            "-It is not what you think! No es lo que tú piensas",
          ],
        },
        {
          palabra: "WHO",
          description: "QUIÉN, QUIÉNES",
          items: [
            "-Who are you? Quién eres tú",
            "-Who are they? ¿Quiénes son ellos?",
            "",
          ],
        },
        {
          palabra: "WHY",
          description: "POR QUÉ",
          items: [
            "Why do you say that?",
            "¿Por qué dices eso?",
            "Because I am mad at you: Porque estoy enojado contigo",
          ],
        },
        {
          palabra: "WHERE",
          description: "DONDE",
          items: ["-Where are you now?", "¿Dónde Estás Ahora?", ""],
        },
        {
          palabra: "WHOSE",
          description: "DE QUIEN",
          items: ["-Whose is this? ¿De quién es esto?", "", ""],
        },
        {
          palabra: "WHEN",
          description: "CUANDO",
          items: ["-When is that? ¿Cuándo es eso?", "", ""],
        },
        {
          palabra: "WHICH",
          description: "Cuál o Cuáles (para escoger)",
          items: [
            "- Which part don`t you manage to understand? ¿Qué parte no logras entender?",
            "",
            "",
          ],
        },
      ],
      mensajeRespuestasP85: "Complete las preguntas",
      respuestasCuestionarioP85: ["B", "A", "C", "C", "A", "A", "B", "B"],
      cuestionarioP85: [
        {
          respuesta: "",
          pregunta: "1. How old are the twins?",
          options: [
            {
              text: "A) 25 seconds",
              value: "A",
              disabled: false,
            },
            {
              text: "B) 8 years old",
              value: "B",
              disabled: false,
            },
            {
              text: "C) 10 minutes",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "2. How many brothers do the twins have?",
          options: [
            {
              text: "A) 1",
              value: "A",
              disabled: false,
            },
            {
              text: "B) 3",
              value: "B",
              disabled: false,
            },
            {
              text: "C) 4",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "3. How fast can Henry run to the corner of the block? ",
          options: [
            {
              text: "A) 25 seconds",
              value: "A",
              disabled: false,
            },
            {
              text: "B) 1km",
              value: "B",
              disabled: false,
            },
            {
              text: "C) 30 seconds",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "4. How long does it take for the twins to walk to school?",
          options: [
            {
              text: "A) 25 seconds",
              value: "A",
              disabled: false,
            },
            {
              text: "B) 8 years old",
              value: "B",
              disabled: false,
            },
            {
              text: "C) 10 minutes",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "5. How often do the twins go to school?",
          options: [
            {
              text: "A) every day",
              value: "A",
              disabled: false,
            },
            {
              text: "B) every 4 days",
              value: "B",
              disabled: false,
            },
            {
              text: "C) from Monday to Thursday",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "6. How far is the school from home?",
          options: [
            {
              text: "A)  1km away",
              value: "A",
              disabled: false,
            },
            {
              text: "B) 40kg",
              value: "B",
              disabled: false,
            },
            {
              text: "C) 10 minutes",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "7. How long does Mary wait before she gets worried?",
          options: [
            {
              text: "A) 25 seconds",
              value: "A",
              disabled: false,
            },
            {
              text: "B) 15 minutes",
              value: "B",
              disabled: false,
            },
            {
              text: "C) 10 minutes",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "8. How much does the dog weight?",
          options: [
            {
              text: "A) 25 kg",
              value: "A",
              disabled: false,
            },
            {
              text: "B) 40kg",
              value: "B",
              disabled: false,
            },
            {
              text: "C) 10 kg",
              value: "C",
              disabled: false,
            },
          ],
        },
      ],
      comprension85: `"Henry and Adara are twins. They are both 8 years old. When they were born their mother, Mary, was
very happy because they were healthy. Henry and Adara have one brother named Ronan. Ronan is 4
years old. Both Henry and Adara are very fast runners, Henry can run from their house to the corner of
the block in less than 30 seconds, but Adara is even faster, she can run to the corner in 25 seconds. They
both have been going to school for 3 years, they go to school 5 days a week. The school is not far away, every day they have school they walk to school. The school is only 1km away and it takes them 10
minutes to walk there. They know how to walk to school without help from their mother Mary because
she taught the twins how to follow the directions to school and to be careful when crossing the
roads. Most days Mary waits for the twins at home with Ronan, if they are over 15 minutes late, she
starts to worry and Mary starts to look for them. Usually it is very easy to find them, they like playing
with the 40 kg dog at the neighbor's house."`,
      palabrasP83: [
        "1. Come on in: Entra",
        "2. Turn the light on: Enciende la Luz",
        "3. Turn the light off: Apaga la luz",
        "4. Sit down, please: Siéntate, por favor",
        "5. Give me five: Dame esos cinco",
        "6. Catch it: Atrápalo",
        "7. Give it to me: Dámelo",
        "8. Pick it up: Recógelo",
        "9. Shut the door: Cierra la puerta",
        "10. Open the door: Abra la puerta",
        "11. Wipe your hands: Limpia tus manos",
        "12. Eat slowly: Come despacio",
        "13. Knock on the door: Toca la puerta",
        "14. Ring the bell: Toca el timbre",
        "15. Move aside: Hazte a un lado",
        "16. Get out of here: vete de aquí",
        "17. Call me later. Llámame más tarde",
        "18. Hang on: Espera un momento",
        "19. Drive me to the airport: Llévame al aeropuerto",
        "20. Put your hands up: manos arriba",
        "21. Drop me off here: déjame aquí",
        "22. Turn around: Voltéate",
        "23. Leave me alone: Déjame solo",
        "24. Don´t touch that: No toques eso",
        "25. Let´s go for a walk: Vamos a dar un paseo",
        "26. Don´t bother me: No me molestes",
      ],
      tablaP84P2: {
        fields: [
          { key: "html", label: "" },
          { key: "complejo1", label: "Completar" },
        ],
        items: [
          {
            complejo1: {
              lista: ["fast"],
              textoA: "How",
              textoD: "do you run?",
              tamano: 18,
            },
            html: "I run fast",
          },
          {
            complejo1: {
              lista: ["old"],
              textoA: "How",
              textoD: "is the baby?",
              tamano: 18,
            },
            html: "The baby is 6 months old",
          },
          {
            complejo1: {
              lista: ["many"],
              textoA: "How",
              textoD: "brothers do you have?",
              tamano: 25,
            },
            html: "I have 2 brothers",
          },
          {
            complejo1: {
              lista: ["often"],
              textoA: "How",
              textoD: "do you play?",
              tamano: 19,
            },
            html: "I play once in a blue moon",
          },
          {
            complejo1: {
              lista: ["about"],
              textoA: "How",
              textoD: "watching a movie tonight?",
              tamano: 27,
            },
            html: "I don’t know what to do",
          },
          {
            complejo1: {
              lista: ["long"],
              textoA: "How",
              textoD: "were you in the office?",
              tamano: 24,
            },
            html: "I was in the office until 3:00 am",
          },
          {
            complejo1: {
              lista: ["easy"],
              textoA: "How",
              textoD: "is that?",
              tamano: 16,
            },
            html: "That is very easy",
          },
          {
            complejo1: {
              lista: ["far"],
              textoA: "How",
              textoD: "do you live from here?",
              tamano: 23,
            },
            html: "My house is up there in the hill. It is 2-hour walk",
          },
          {
            complejo1: {
              lista: ["much"],
              textoA: "How",
              textoD: "do you love me?",
              tamano: 21,
            },
            html: "I love you very much",
          },
          {
            complejo1: {
              lista: ["long"],
              textoA: "How",
              textoD: "do you work a day?",
              tamano: 23,
            },
            html: "I work for 10 hours a day",
          },
          {
            complejo1: {
              lista: ["fast"],
              textoA: "How",
              textoD: "do you run?",
              tamano: 18,
            },
            html: "I felt very good last night",
          },
        ],
      },
      tablaP84: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "html", label: "How", thClass: "Yelow" },
          { key: "como", label: "Cómo", thClass: "Red" },
          { key: "areyou", label: "How are you?", thClass: "Blue" },
          {
            key: "comoestas",
            label: "¿Cómo estás?",
            thClass: "Blue2",
          },
        ],
        items: [
          {
            html: "<h6><strong>How old</strong></h6>",
            como: "De qué edad",
            areyou: "How old are you?",
            comoestas: "¿De qué edad eres tú?",
          },
          {
            html: "<h6><strong>How many</strong></h6>",
            como: "Cuántos (as)",
            areyou: "How many people fit in a taxi?",
            comoestas: "¿Cuántas personas caben en un taxi?",
          },
          {
            html: "<h6><strong>How fast</strong></h6>",
            como: "Qué tan rápido, a qué velocidad",
            areyou: "How fast does this car go?",
            comoestas: "¿Qué tan rápido anda este carro?",
          },
          {
            html: "<h6><strong>How long</strong></h6>",
            como: "Cuánto tiempo",
            areyou: "How long does it take?",
            comoestas: "¿Cuánto tiempo tarda?",
          },
          {
            html: "<h6><strong>How come</strong></h6>",
            como: "Por qué",
            areyou: "How come you are crying?",
            comoestas: "¿Por qué estás llorando?",
          },
          {
            html: "<h6><strong>How much</strong></h6>",
            como: "Cuánto (o)",
            areyou: "How much is this?",
            comoestas: "¿Cuánto cuesta esto?",
          },
          {
            html: "<h6><strong>How often</strong></h6>",
            como: "Con qué frecuencia",
            areyou: "How often do you visit the doctor?",
            comoestas: "¿Con que frecuencia visitas al doctor?",
          },
          {
            html: "<h6><strong>How far</strong></h6>",
            como: "Qué tan lejos",
            areyou: "How far is it?",
            comoestas: "¿Qué tan lejos está?",
          },
          {
            html: "<h6><strong>How about</strong></h6>",
            como: "Qué tal si",
            areyou: "How about watching a movie?",
            comoestas: "¿Qué tal ver una película?",
          },
          {
            html: "<h6><strong>How late</strong></h6>",
            como: "Qué tan tarde",
            areyou: "How late can you be here?",
            comoestas: "¿Qué tan tarde puedes estar aquí?",
          },
          {
            html: "<h6><strong>How well</strong></h6>",
            como: "Qué tan bien",
            areyou: "How well do you play?",
            comoestas: "¿Qué tan bien juegas?",
          },
          {
            html: "<h6><strong>How easy</strong></h6>",
            como: "Qué tan fácil",
            areyou: "How easy is that?",
            comoestas: "¿Qué tan fácil es eso?",
          },
        ],
      },
    };
  },
};
</script>

<style scoped>
#textPractice {
  text-align: left;
  margin-bottom: 1em;
  font-size: 1.5em;
}
/deep/.labelPregunta {
  font-weight: bold;
}

/deep/ #tabla {
  padding-right: 0px;
  padding-left: 0px;
}
/deep/ .row {
  width: 100%;
  margin: 0;
  margin-bottom: 1em;
  padding: 0;
}

/deep/ #EnglishInput,
#SpanishInput {
  width: 100%;
}

/deep/ .colorText {
  color: white;
}

/deep/ .Blue {
  background-color: #002060;
  color: white;
}
/deep/ .Red {
  background-color: crimson;
  color: white;
}
/deep/ .Yelow {
  background-color: #ffc000;
  color: white;
}
/deep/ .Green {
  background-color: chartreuse;
}
/deep/ .Blue2 {
  background-color: #00b0f0;
  color: white;
}

/deep/ .noHead {
  border-width: 0;
  font-size: 0;
}

/deep/.colorLetraRojo {
  color: red;
  margin-left: 8px;
  margin-right: 8px;
}

#cuadroTexto {
  margin-bottom: 1em;
}

img {
  width: 100%;
}

/deep/ #textRequired {
  width: 200px;
}

/deep/ #inputText {
  margin: 0;
  display: inline-flex;
}

#titulo {
  color: red;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 1.5em;
}

#subTitulo {
  padding: 0;
  margin-right: auto;
  color: darkcyan;
  margin-top: 1.5em;
  text-align: left;
}

#textoCompromiso {
  text-align: left;
  margin-bottom: 1em;
  font-size: 1.5em;
}

.textList {
  font-size: 1.5em;
}

#numeroMagico2,
#numeroMagico4,
#numeroMagico5,
#numeroMagico12 {
  background-color: salmon;
  margin-right: auto;
  margin-left: auto;
  padding-top: 0.5em;
  padding-bottom: 0.5em;
  border-style: solid;
  border-radius: 1em;
  border-color: black;
  font-size: 1.5em;
  color: black;
  font-family: "PT Sans";
  font-weight: bold;
  margin-bottom: auto;
}
#numeroMagico2 {
  background: greenyellow;
}

#numeroMagico4 {
  background: red;
}
#numeroMagico5 {
  background: royalblue;
}
#numeroMagico12 {
  background: cadetblue;
}
</style>