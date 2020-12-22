<template>
  <div>
    <div class="row">
      <h3 id="subTitulo">ALGUNOS VERBOS TIENEN SU PROPIA PREPOSICIÓN.</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <p class="parrafo">
          Aunque en español, no tenga sentido la traducción debemos aprenderlos
          de este modo.
        </p>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div class="col-sm-12">
          <b-card>
            <p class="parrafoTabla">
              <tablaTC :cuestionario="tablaP91" />
            </p>
          </b-card>
        </div>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">PRACTICE</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <p class="parrafo">Completa con la preposición correcta</p>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6" id="text">
        <opcionMultiple
          :options="$data.cuestionarioP92"
          :rEsperadas="$data.respuestasCuestionarioP92"
          @respuestas="$data.mensajeRespuestasP92 = $event"
        />
      </div>
      <b-modal ref="my-modalP92" hide-footer title="RESULTADO">{{
        mensajeRespuestasP92
      }}</b-modal>
      <div class="col-sm-1"></div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-3">
        <b-button variant="primary" @click="showModal('my-modalP92')"
          >VERIFICAR PREGUNTAS</b-button
        >
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">SUJETOS Y OBJETOS EN INGLÉS</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <p class="parrafo">
          Los sujetos tienen objetos y estos siempre van después del verbo,
          aunque algunas veces signifiquen lo mismo. Después de un verbo no se
          usan los sujetos. Veamos algunos errores comunes:
        </p>
        <h5 class="parrafo">
          <p>
            - I love
            <span class="colorLetraRojo">
              she
              <strong>X</strong>
            </span>
          </p>
          <p>
            - This is for
            <span class="colorLetraRojo">
              he
              <strong>X</strong>
            </span>
          </p>
          <p>
            - My teacher told
            <span class="colorLetraRojo">
              we
              <strong>X</strong>
            </span>
          </p>
        </h5>
        <p class="parrafo">
          Nota: Los tres anteriores ejemplos son incorrectos porque después de
          un verbo no se usan sujetos. En ingles cada sujeto tiene un objecto
          que es usado después de los verbos. Sobre quien recae la acción.
        </p>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div class="col-sm-4">
          <b-card>
            <p class="parrafoTabla">
              <tablaTC :cuestionario="tablaP93" />
            </p>
          </b-card>
        </div>
        <div class="col-sm-4">
          <h3 class="colorLetraRojo">Siempre después del verbo →</h3>
        </div>
        <div class="col-sm-4">
          <b-card>
            <p class="parrafoTabla">
              <tablaTC :cuestionario="tablaP93P2" />
            </p>
          </b-card>
        </div>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <p class="parrafo">ESTUDIEMOS ESTOS EJEMPLOS</p>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <b-card>
          <p class= "parrafoTabla">
            <listaIndex :tabla="tablaP93B" />
          </p>
        </b-card>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">PRACTICE</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <p class="parrafo">
          Completa con el objeto o sujeto de acuerdo a la oración.
        </p>
      </div>
    </div>

    <div class="row" v-for="(item, index) in preguntasCompletarP93.items">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <div class="col-sm-1">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP93.nombre + index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
            :tamano="item.tamano"
          />
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
      preguntasCompletarP93: {
        nombre: "preguntasCompletarP24",
        items: [
          {
            esperado: ["them"],
            textoA: "1.   My life depends on",
            textoD: "(them-they)",
            tamano: 30,
          },
          {
            esperado: ["her"],
            textoA: "2. I don´t know",
            textoD: "(her-she)",
            tamano: 23,
          },
          {
            esperado: ["they"],
            textoA: "3. What are",
            textoD: "going to do? (them-they)",
            tamano: 31,
          },
          {
            esperado: ["him"],
            textoA: "4. You shouldn´t look at",
            textoD: "(him-he)",
            tamano: 28,
          },
          {
            esperado: ["me"],
            textoA: "5. You don´t know",
            textoD: "(I-me)",
            tamano: 23,
          },
          {
            esperado: ["us"],
            textoA: "6. They need ",
            textoD: "(we-us)",
            tamano: 21,
          },
          {
            esperado: ["her"],
            textoA: "7. I saw",
            textoD: "(she-her)",
            tamano: 19,
          },
        ],
      },
      mensajeRespuestasP92: "Complete las preguntas",
      respuestasCuestionarioP92: [
        "B",
        "A",
        "A",
        "B",
        "C",
        "A",
        "A",
        "B",
        "C",
        "A",
        "B",
        "C",
        "B",
        "C",
      ],
      cuestionarioP92: [
        {
          respuesta: "",
          pregunta:
            "1. I am interested ____ studying English (Estoy interesado en estudiar)",
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion23/audio/pag92/AC1P91R15n1.mp3",
          options: [
            {
              text: "A) On",
              value: "A",
              disabled: false,
            },
            {
              text: "B) in",
              value: "B",
              disabled: false,
            },
            {
              text: "C) at",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "2. I don’t want to talk ____ you (Yo no quiero hablar contigo)",
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion23/audio/pag92/AC1P91R16n2.mp3",
          options: [
            {
              text: "A) To",
              value: "A",
              disabled: false,
            },
            {
              text: "B) with",
              value: "B",
              disabled: false,
            },
            {
              text: "C) of",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "3. He yelled ____ the dog for peeing on the carpet (Él gritó al perro por orinarse en la alfombra ",
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion23/audio/pag92/AC1P91R17n3.mp3",
          options: [
            {
              text: "A) at",
              value: "A",
              disabled: false,
            },
            {
              text: "B) in",
              value: "B",
              disabled: false,
            },
            {
              text: "C) for",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "4. Who did you fall in love ____? (¿De quién te enamoraste?)",
          audio:"https://classroom.pikinglish.com/cursos/curso1/leccion23/audio/pag92/AC1P91R18n4.mp3",
          options: [
            {
              text: "A) Of",
              value: "A",
              disabled: false,
            },
            {
              text: "B) with",
              value: "B",
              disabled: false,
            },
            {
              text: "C) for",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "5. I have come to say good bye ___ you (He venido a despedirme de ti)",
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion23/audio/pag92/AC1P91R19n5.mp3",
          options: [
            {
              text: "A) Of",
              value: "A",
              disabled: false,
            },
            {
              text: "B) in",
              value: "B",
              disabled: false,
            },
            {
              text: "C) to",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "6. How much do you think ____her? (¿Cuánto piensas en ella?)",
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion23/audio/pag92/AC1P91R20n6.mp3",
          options: [
            {
              text: "A) Of",
              value: "A",
              disabled: false,
            },
            {
              text: "B) in",
              value: "B",
              disabled: false,
            },
            {
              text: "C) for",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "7. I have realized I depend _____ my parents for emotional support",
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion23/audio/pag92/AC1P91R21n7.mp3",
          options: [
            {
              text: "A) On",
              value: "A",
              disabled: false,
            },
            {
              text: "B) in",
              value: "B",
              disabled: false,
            },
            {
              text: "C) for",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "8. You have to stop lying ____ me",
          audio:"https://classroom.pikinglish.com/cursos/curso1/leccion23/audio/pag92/AC1P91R22n8.mp3",
          options: [
            {
              text: "A) Of",
              value: "A",
              disabled: false,
            },
            {
              text: "B) to",
              value: "B",
              disabled: false,
            },
            {
              text: "C) at",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "9. I am calling to congratulate you ______ your wedding",
          audio:"https://classroom.pikinglish.com/cursos/curso1/leccion23/audio/pag92/AC1P91R23n9.mp3",
          options: [
            {
              text: "A) Of",
              value: "A",
              disabled: false,
            },
            {
              text: "B) to",
              value: "B",
              disabled: false,
            },
            {
              text: "C) on",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "10. We arrived _____ Chicago last night",
          audio:"https://classroom.pikinglish.com/cursos/curso1/leccion23/audio/pag92/AC1P91R24n10.mp3",
          options: [
            {
              text: "A) In",
              value: "A",
              disabled: false,
            },
            {
              text: "B) to",
              value: "B",
              disabled: false,
            },
            {
              text: "C) at",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "11. Have you ever been ____ Niagara Falls?",
          audio:"https://classroom.pikinglish.com/cursos/curso1/leccion23/audio/pag92/AC1P91R25n11.mp3",
          options: [
            {
              text: "A) Of",
              value: "A",
              disabled: false,
            },
            {
              text: "B) to",
              value: "B",
              disabled: false,
            },
            {
              text: "C) at",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "12. Can you wait _____ Matt? -he will be here soon",
          audio:"https://classroom.pikinglish.com/cursos/curso1/leccion23/audio/pag92/AC1P91R26n12.mp3",
          options: [
            {
              text: "A) Of",
              value: "A",
              disabled: false,
            },
            {
              text: "B) to",
              value: "B",
              disabled: false,
            },
            {
              text: "C) for",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "13. Have you ever listened ____ the lyrics of 'Stairway to Heaven'?",
            audio:"https://classroom.pikinglish.com/cursos/curso1/leccion23/audio/pag92/AC1P91R27n13.mp3",
          options: [
            {
              text: "A) Of",
              value: "A",
              disabled: false,
            },
            {
              text: "B) to",
              value: "B",
              disabled: false,
            },
            {
              text: "C) at",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "14. We will arrive ____ your house in twenty (20) minutes",
          audio:"https://classroom.pikinglish.com/cursos/curso1/leccion23/audio/pag92/AC1P91R28n14.mp3",
          options: [
            {
              text: "A) Of",
              value: "A",
              disabled: false,
            },
            {
              text: "B) to",
              value: "B",
              disabled: false,
            },
            {
              text: "C) at",
              value: "C",
              disabled: false,
            },
          ],
        },
      ],
      tablaP93: {
        fields: [
          { key: "subjects", label: "SUBJECTS" },
          { key: "spanish", label: "SPANISH" },
        ],
        items: [
          {
            subjects: "I",
            spanish: "Yo",
          },
          {
            subjects: "YOU",
            spanish: "Tú-ustedes",
          },
          {
            subjects: "SHE",
            spanish: "Ella",
          },
          {
            subjects: "HE",
            spanish: "El",
          },
          {
            subjects: "IT",
            spanish: "Sin traducción",
          },
          {
            subjects: "THEY",
            spanish: "Ellos-ellas",
          },
          {
            subjects: "WE",
            spanish: "Nosotros-nosotras",
          },
        ],
      },
      tablaP93B: {
        fields: [
          { key: "html", label: "ESPAÑOL" },
          { key: "html2", label: "FORMA INCORRECTA" },
          { key: "html3", label: "FORMA CORRECTA" },
        ],
        bordered: true,
        items: [
          {
            html: "<p class= parrafoTabla>YO <span class='colorLetraRojo'>LA</span> AMO</h5>",
            html2: "<p class= parrafoTabla>I LOVE SHE</p>",
            html3: "<p class= parrafoTabla>I LOVE HER</p>",
          },
          {
            html:
              "<p class= parrafoTabla> NOSOTROS <span class='colorLetraRojo'>LOS</span> AMAMOS </p>",
            html2: "<p class= parrafoTabla>WE LOVE THEY</p>",
            html3: "<p class= parrafoTabla>WE LOVE THEM</p>",
          },
          {
            html:
              "<p class= parrafoTabla>ESTO ES PARA <span class='colorLetraRojo'>ÉL</span></p>",
            html2: "<p class= parrafoTabla>THIS IS FOR HER</p>",
            html3: "<p class= parrafoTabla>THIS IS FOR HIM</p>",
          },
        ],
      },
      tablaP93P2: {
        fields: [{ key: "objects", label: "OBJECTS" }],
        items: [
          {
            objects: "ME",
          },
          {
            objects: "YOU",
          },
          {
            objects: "HER",
          },
          {
            objects: "HIM",
          },
          {
            objects: "IT",
          },
          {
            objects: "THEM",
          },
          {
            objects: "US",
          },
        ],
      },
      tablaP91: {
        fields: [
          { key: "spanish", label: "Spanish", thClass: "Yelow" },
          { key: "english", label: "English", thClass: "Blue" },
          { key: "english2", label: "Example", thClass: "Blue2" },
        ],
        items: [
          {
            english2: "I think of you",
            english: "Think of/ think about",
            spanish: "Pensar en",
          },
          {
            english2: "I fell in love with you",
            english: "Fall in love with",
            spanish: "Enamorase de",
          },
          {
            english2: "I depend on your decision",
            english: "Depend on",
            spanish: "Depender de",
          },
          {
            english2: "I need to talk to you",
            english: "Talk to",
            spanish: "Hablar con",
          },
          {
            english2: "Listen to me",
            english: "Listen to",
            spanish: "Escuchar",
          },
          {
            english2: "What did you say to Victor?",
            english: "Say to",
            spanish: "Decir",
          },
          {
            english2: "Don´t lie to me",
            english: "Lie to",
            spanish: "Mentir",
          },
          {
            english2: "She yelled at me",
            english: "Yell at",
            spanish: "Gritar",
          },
          {
            english2:
              "I want to congratulate you on your dedication and discipline",
            english: "Congratulate on",
            spanish: "Felicitar po",
          },
          {
            english2: "Wait for me at the corner",
            english: "Wait for",
            spanish: "Esperar a",
          },
          {
            english2: "I arrived in Paris at 3am",
            english: " Arrive in",
            spanish: "Llegar a (ciudades o países)",
          },
          {
            english2: "I arrived at school late",
            english: "Arrive at",
            spanish: "Llegar a (un lugar dentro de la ciudad)",
          },
          {
            english2: "Which countries have you been to?",
            english: "Been to",
            spanish: "Estado en (lugar)",
          },
          {
            english2: "I was interested in you",
            english: "Interested in",
            spanish: "Interesado en",
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