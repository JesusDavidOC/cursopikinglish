<template>
  <div>
    <div class="row">
      <h3 id="subTitulo">COMMON QUESTION</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div
          class="col-sm-2"
          v-for="item in $data.tablasTiempoP87"
          style="margin:0; padding:0; text-align: left"
        >
          <listaIndex :tabla="item" />
        </div>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <tablaTC
          id="diiv"
          class="overflow-auto"
          :cuestionario="$data.cuestionario1"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">PREGUNTAS CON PREPOSICIONES</h3>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h5 style="text-align: justify">
          Son preguntas del español que inician con las siguientes
          palabras
          <strong>En, para, sobre, de, con, hacia, etc.</strong> En inglés estás
          palabras van después del verbo.
        </h5>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <listaIndex :tabla="tablaP79P2" />
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">COMMON QUESTION</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div
          class="col-sm-2"
          v-for="item in $data.tablasTiempoP88"
          style="margin:0; padding:0; text-align: left"
        >
          <listaIndex :tabla="item" />
        </div>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <tablaTC
          id="diiv"
          class="overflow-auto"
          :cuestionario="$data.cuestionario2"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h5 style="text-align: justify">
          Complete las preguntas con la preposición correcta.
          Of-With-About-In-From-For
        </h5>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div class="col-sm-12">
          <tablaTC :cuestionario="tablaP89" />
        </div>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">LAS PREPOSICIONES EN INGLÉS</h3>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h5 style="text-align: justify">
          Son palabras para determinar la posición, o tiempo o manera de un objeto o persona y además para
          acompañar a un verbo.
        </h5>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <listaIndex :tabla="$data.tablaA" />
      <div class="col-sm-1"></div>
      <listaIndex :tabla="$data.tablaB" />
    </div>

    <div class="row">
      <h3 id="subTitulo">PRACTICE</h3>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h5 style="text-align: justify">
          Completar la oración con la preposición correcta
        </h5>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6" id="text">
        <opcionMultiple
          :options="$data.cuestionarioP90"
          :rEsperadas="$data.respuestasCuestionarioP90"
          @respuestas="$data.mensajeRespuestasP90 = $event"
        />
      </div>
      <b-modal ref="my-modalP90" hide-footer title="RESULTADO">{{mensajeRespuestasP90 }}</b-modal>
      <div class="col-sm-1"></div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-3">
        <b-button variant="primary" @click="showModal('my-modalP90')">VERIFICAR PREGUNTAS</b-button>
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
      mensajeRespuestasP90: "Complete las preguntas",
      respuestasCuestionarioP90: [
        "C",
        "B",
        "A",
        "B",
        "A",
        "C",
        "B",
        "A",
        "A",
        "C",
        "A",
        "B",
        "B",
        "A",
        "C",
        "A",
      ],
      cuestionarioP90: [
        {
          respuesta: "",
          pregunta: "1. This house is made ____ wood",
          options: [
            {
              text: "A) in",
              value: "A",
              disabled: false,
            },
            {
              text: "B) for",
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
            "2. I live ____ my parents",
          options: [
            {
              text: "A) in",
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
          pregunta: "3. The bank is _______ the casino and the pharmacy ",
          options: [
            {
              text: "A) between",
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
          pregunta: "4. Thank you _____ helping me",
          options: [
            {
              text: "A) in",
              value: "A",
              disabled: false,
            },
            {
              text: "B) for",
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
            "5. I swam ____ the river yesterday",
          options: [
            {
              text: "A) in",
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
          pregunta: "6. I always go home _____ classes",
          options: [
            {
              text: "A) up",
              value: "A",
              disabled: false,
            },
            {
              text: "B) with",
              value: "B",
              disabled: false,
            },
            {
              text: "C) after",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "7. I put the broom ______ the door",
          options: [
            {
              text: "A) in",
              value: "A",
              disabled: false,
            },
            {
              text: "B) behind",
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
            "8. I wrote a book _______ learning English",
          options: [
            {
              text: "A) about",
              value: "A",
              disabled: false,
            },
            {
              text: "B) with",
              value: "B",
              disabled: false,
            },
            {
              text: "C) out",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "9. The dog is ______ the table",
          options: [
            {
              text: "A) under",
              value: "A",
              disabled: false,
            },
            {
              text: "B) about",
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
            "10. Show me what you are made _____",
          options: [
            {
              text: "A) In",
              value: "A",
              disabled: false,
            },
            {
              text: "B) up",
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
            "11. . Please go ______ stairs to answer the door",
          options: [
            {
              text: "A) down",
              value: "A",
              disabled: false,
            },
            {
              text: "B) across",
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
            "12. The sun comes ____ in the morning",
          options: [
            {
              text: "A) along",
              value: "A",
              disabled: false,
            },
            {
              text: "B) up",
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
            "13. Get _____ of the car",
          options: [
            {
              text: "A) for",
              value: "A",
              disabled: false,
            },
            {
              text: "B) out",
              value: "B",
              disabled: false,
            },
            {
              text: "C) with",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "14. I work 5 days a week, ______ Monday to Friday",
          options: [
            {
              text: "A) from",
              value: "A",
              disabled: false,
            },
            {
              text: "B) up",
              value: "B",
              disabled: false,
            },
            {
              text: "C) with",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "15. She kicked the ball ______ the field",
          options: [
            {
              text: "A) of",
              value: "A",
              disabled: false,
            },
            {
              text: "B) with",
              value: "B",
              disabled: false,
            },
            {
              text: "C) across",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "I called her ______ she arrived",
          options: [
            {
              text: "A) before",
              value: "A",
              disabled: false,
            },
            {
              text: "B) in",
              value: "B",
              disabled: false,
            },
            {
              text: "C) with",
              value: "C",
              disabled: false,
            },
          ],
        },
      ],
      tablaA: {
        bordered: true,
        camposInput: false,
        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "English", thClass: "Blue" },
          { key: "Spanish", thClass: "Red" },
        ],
        items: [
          { English: "Of", Spanish: "De" },
          { English: "With", Spanish: "Con" },
          { English: "At", Spanish: "En el, a las" },
          { English: "For", Spanish: "Por, para" },
          { English: "In", Spanish: "En" },
          { English: "On", Spanish: "Sobre" },
          { English: "From", Spanish: "De, desde" },
          { English: "About", Spanish: "Acerca de, sobre, de" },
          { English: "To", Spanish: "Para, a" },
          { English: "Between", Spanish: "En medio de" },
        ],
      },
      tablaB: {
        bordered: true,
        camposInput: false,
        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "English", thClass: "Blue" },
          { key: "Spanish", thClass: "Red" },
        ],
        items: [
          { English: "Up", Spanish: "Arriba" },
          { English: "Down", Spanish: "Abajo" },
          { English: "By", Spanish: "a más tardar, al lado de, por" },
          { English: "Out", Spanish: "Afuera" },
          { English: "Over", Spanish: "Encima de, durante" },
          { English: "Under", Spanish: "Debajo de" },
          { English: "Along", Spanish: "a lo largo de" },
          { English: "Across", Spanish: "A través de" },
          { English: "After", Spanish: "Después, después de" },
          { English: "Before", Spanish: "Antes de, antes, ante" },
        ],
      },
      tablaP89: {
        fields: [
          { key: "html", label: "Español" },
          { key: "complejo1", label: "English" },
        ],
        items: [
          {
            complejo1: {
              lista: ["with"],
              textoA: "Who are you living",
              textoD: "?",
              tamano: 20,
            },
            html: "¿Con quién estás viviendo?",
          },
          {
            complejo1: {
              lista: ["in"],
              textoA: "What are you interested",
              textoD: "?",
              tamano: 22,
            },
            html: "¿En qué estás interesado?",
          },
          {
            complejo1: {
              lista: ["from"],
              textoA: "Where did you get that",
              textoD: "?",
              tamano: 23,
            },
            html: "¿De dónde sacaste eso?",
          },
          {
            complejo1: {
              lista: ["about"],
              textoA: "What are you talking",
              textoD: "?",
              tamano: 22,
            },
            html: "¿Sobre qué estás hablando?",
          },
          {
            complejo1: {
              lista: ["for"],
              textoA: "Who do you work",
              textoD: "?",
              tamano: 19,
            },
            html: "¿Para quién trabajas?",
          },
          {
            complejo1: {
              lista: ["of"],
              textoA: "What is this made",
              textoD: "?",
              tamano: 19,
            },
            html: "¿De qué está hecho esto?",
          },
          {
            complejo1: {
              lista: ["with"],
              textoA: "Who are you traveling",
              textoD: "?",
              tamano: 22,
            },
            html: "¿Con quién estás viajando?",
          },
          {
            complejo1: {
              lista: ["from"],
              textoA: "Where did you get that idea",
              textoD: "?",
              tamano: 25,
            },
            html: "¿De dónde sacaste esa idea?",
          },
          {
            complejo1: {
              lista: ["about"],
              textoA: "Who are you talking",
              textoD: "?",
              tamano: 22,
            },
            html: "¿De quién estás hablando?",
          },
        ],
      },
      
      tablaP79P2: {
        fields: [
          { key: "html", label: "SPANISH", thClass: "Yelow" },
          { key: "english", label: "ENGLISH", thClass: "Red" },
        ],
        bordered: true,
        items: [
          {
            html:
              "<h6> <span style='color: red;'>¿DE</span> donde está viniendo ese humo? </h6>",
            english: "Where is that smoke coming FROM?",
          },
          {
            html:
              "<h6> <span style='color: red;'>¿SOBRE/ ACERCA DE/ DE</span> que estás hablando? </h6>",
            english: "What are you talking ABOUT?",
          },
          {
            html:
              "<h6> <span style='color: red;'>¿PARA</span> quién trabajas?</h6>",
            english: "Who do you work FOR?",
          },
          {
            html:
              "<h6> <span style='color: red;'>¿Con</span> quién saliste anoche? </h6>",
            english: "Who did you go out WITH last night?",
          },
          {
            html:
              "<h6> <span style='color: red;'>¿De</span> qué está hecho eso?</h6>",
            english: "What is that made OF?",
          },
          {
            html: "<h6> <span style='color: red;'>¿De</span> dónde eres? </h6>",
            english: "Where are you FROM?",
          },
          {
            html:
              "<h6> <span style='color: red;'>¿En qué</span> estás interesado? </h6>",
            english: "What are you interested IN?",
          },
          {
            html:
              "<h6> <span style='color: red;'>¿Hacia</span> dónde va este bus? </h6>",
            english: "Where does this bus go TO?",
          },
          {
            html:
              "<h6> <span style='color: red;'>¿Con</span> quién está hablando? </h6>",
            english: "Who are you talking TO?",
          },
        ],
      },
      cuestionario1: {
        fields: [
          { key: "A", thClass: "Blue" },
          { key: "B", thClass: "Red" },
          { key: "C", thClass: "Yelow" },
          { key: "D", thClass: "Green" },
          { key: "E", thClass: "Blue2" },
          { key: "complejo1", label: "ENGLISH" },
          { key: "español", label: "SPANISH" },
        ],
        items: [
          {
            A: 1,
            B: 1,
            C: 2,
            D: 8,
            E: "",
            complejo1: { lista: ["What are you doing?"] },
            español: "¿Qué estás haciendo?",
          },
          {
            A: 3,
            B: 4,
            C: 2,
            D: 9,
            E: 8,
            complejo1: { lista: ["Where would you like to go?"] },
            español: "¿Dónde te gustaría ir?",
          },
          {
            A: 1,
            B: 7,
            C: 5,
            D: "",
            E: 6,
            complejo1: { lista: ["What can I do for you?"] },
            español: "¿Qué puedo hacer por ti?",
          },
          {
            A: 4,
            B: 8,
            C: 7,
            D: "",
            E: 4,
            complejo1: { lista: ["How was your day?"] },
            español: "¿Cómo estuvo tu día?",
          },
          {
            A: 1,
            B: 1,
            C: 4,
            D: 12,
            E: 1,
            complejo1: { lista: ["What are we going to do now?"] },
            español: "¿Qué vamos a hacer ahora?",
          },
          {
            A: 5,
            B: 1,
            C: 2,
            D: 7,
            E: "",
            complejo1: { lista: ["When are you coming?"] },
            español: "¿Cuándo vas a venir?",
          },
          {
            A: 4,
            B: 1,
            C: 2,
            D: 8,
            E: "",
            complejo1: { lista: ["How are you doing?"] },
            español: "¿Cómo te va?",
          },
          {
            A: 1,
            B: 3,
            C: 2,
            D: 11,
            E: "",
            complejo1: { lista: ["What do you mean?"] },
            español: "¿Qué quieres decir?",
          },
          {
            A: "",
            B: 1,
            C: 2,
            D: 6,
            E: "",
            complejo1: { lista: ["Are you going?"] },
            español: "¿Vas a ir?",
          },
          {
            A: 4,
            B: 3,
            C: 2,
            D: 9,
            E: 7,
            complejo1: { lista: ["How do you like it?"] },
            español: "¿Cómo te gusta?",
          },
          {
            A: 6,
            B: 5,
            C: 2,
            D: 9,
            E: 3,
            complejo1: {
              lista: ["What time would you like something to drink?"],
            },
            español: "¿A qué horas te gustaría algo de beber?",
          },
          {
            A: 6,
            B: 5,
            C: 3,
            D: 3,
            E: 7,
            complejo1: { lista: ["What time will she have it?"] },
            español: "¿A qué horas ella lo tendrá?",
          },
          {
            A: 1,
            B: 2,
            C: 3,
            D: 8,
            E: "",
            complejo1: { lista: ["What is she doing?"] },
            español: "¿Qué está ella haciendo?",
          },
          {
            A: 3,
            B: 1,
            C: 2,
            D: 6,
            E: "",
            complejo1: { lista: ["Where are you going?"] },
            español: "¿Para dónde vas?",
          },
          {
            A: "",
            B: 3,
            C: 2,
            D: 3,
            E: 5,
            complejo1: { lista: ["Do you have any money?"] },
            español: "¿Tú tienes algo de dinero?",
          },
          {
            A: 1,
            B: 2,
            C: 7,
            D: 1,
            E: "",
            complejo1: { lista: ["What is your name?"] },
            español: "¿Cuál es tu nombre?",
          },
          {
            A: 3,
            B: 1,
            C: 2,
            D: 2,
            E: "",
            complejo1: { lista: ["Where are you from?"] },
            español: "¿De dónde eres?",
          },
          {
            A: 1,
            B: 1,
            C: 2,
            D: 12,
            E: 1,
            complejo1: { lista: ["What are you going to do now?"] },
            español: "¿Qué vas a hacer ahora?",
          },
          {
            A: "",
            B: 4,
            C: 2,
            D: 9,
            E: 3,
            complejo1: { lista: ["Would you like something to drink?"] },
            español: "¿Te gustaría algo de beber?",
          },
          {
            A: 4,
            B: 8,
            C: 7,
            D: "",
            E: 4,
            complejo1: { lista: ["How was your day?"] },
            español: "¿Cómo estuvo tu día?",
          },
          {
            A: 1,
            B: 3,
            C: 2,
            D: 11,
            E: "",
            complejo1: { lista: ["What do you mean?"] },
            español: "¿Qué quieres decir?",
          },
          {
            A: 5,
            B: 5,
            C: 2,
            D: 3,
            E: 5,
            complejo1: { lista: ["When will you have any money?"] },
            español: "¿Cuándo tendrás algo de dinero?",
          },
        ],
      },
      cuestionario2: {
        fields: [
          { key: "A", thClass: "Blue" },
          { key: "B", thClass: "Red" },
          { key: "C", thClass: "Yelow" },
          { key: "D", thClass: "Green" },
          { key: "E", thClass: "Blue2" },
          { key: "complejo1", label: "ENGLISH" },
          { key: "español", label: "SPANISH" },
        ],
        items: [
          {
            A: 3,
            B: 6,
            C: 2,
            D: 2,
            E: 6,
            complejo1: { lista: ["who should I go out with?"] },
            español: "¿Con quién debería salir?",
          },
          {
            A: 3,
            B: 4,
            C: 4,
            D: 10,
            E: 5,
            complejo1: { lista: ["Who will she work for?"] },
            español: "¿Para quién ella trabajará?",
          },
          {
            A: 4,
            B: 3,
            C: 1,
            D: 4,
            E: "",
            complejo1: { lista: ["Why did you come?"] },
            español: "¿Por qué viniste?",
          },
          {
            A: 3,
            B: 7,
            C: 1,
            D: 9,
            E: 4,
            complejo1: { lista: ["Who are you thinking about?"] },
            español: "¿En quién estás pensando?",
          },
          {
            A: 1,
            B: 8,
            C: 5,
            D: "",
            E: 5,
            complejo1: { lista: ["What is it for?"] },
            español: "¿Para qué es?",
          },
          {
            A: 1,
            B: 8,
            C: 4,
            D: 9,
            E: 4,
            complejo1: { lista: ["What is she thinking about?"] },
            español: "¿En qué esta ella pensando?",
          },
          {
            A: 2,
            B: 1,
            C: 1,
            D: 4,
            E: 1,
            complejo1: { lista: ["Where do you come from?"] },
            español: "¿De dónde vienes?",
          },
          {
            A: 3,
            B: 5,
            C: 1,
            D: 6,
            E: 2,
            complejo1: { lista: ["Who would you live with?"] },
            español: "¿Con quién vivirías?",
          },
          {
            A: 3,
            B: 1,
            C: 1,
            D: 10,
            E: 5,
            complejo1: { lista: ["Who do you work for?"] },
            español: "¿Para quién trabajas?",
          },
          {
            A: 3,
            B: 3,
            C: 3,
            D: 1,
            E: 2,
            complejo1: { lista: ["Who did he eat with?"] },
            español: "¿Con quién comió él?",
          },
          {
            A: 1,
            B: 7,
            C: 1,
            D: 9,
            E: 4,
            complejo1: { lista: ["What are you thinking about?"] },
            español: "¿En qué estás pensando?",
          },
        ],
      },
      tablasTiempoP88: [
        {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "Z", label: "A", thClass: "colorLetraRojo" },
          ],
          items: [
            { Z: "1. What" },
            { Z: "2. Where" },
            { Z: "3. Who" },
            { Z: "4. Why" },
            { Z: "5. When" },
            { Z: "6. What time" },
            { Z: "7.How" },
          ],
        },
        {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "Z", label: "B", thClass: "colorLetraRojo" },
          ],
          items: [
            { Z: "1. Do" },
            { Z: "2. Does" },
            { Z: "3. Did" },
            { Z: "4. Will" },
            { Z: "5. Would" },
            { Z: "6. Should" },
            { Z: "7. Are" },
            { Z: "8. Is" },
          ],
        },
        {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              label: "C",
              thClass: "colorLetraRojo",
            },
          ],
          items: [
            { Z: "1. You" },
            { Z: "2. I" },
            { Z: "3. He" },
            { Z: "4. She" },
            { Z: "5. It" },
            { Z: "6. We" },
            { Z: "7. They" },
          ],
        },
        {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              label: "D",
              thClass: "colorLetraRojo",
            },
          ],
          items: [
            { Z: "1. Eat" },
            { Z: "2. Go" },
            { Z: "3. See" },
            { Z: "4. Come" },
            { Z: "5. Like" },
            { Z: "6. Live" },
            { Z: "7. Feel" },
            { Z: "8. Talking" },
            { Z: "9.Thinking" },
            { Z: "10.Work" },
          ],
        },
        {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              label: "E",
              thClass: "colorLetraRojo",
            },
          ],
          items: [
            { Z: "1. From" },
            { Z: "2. With" },
            { Z: "3. To" },
            { Z: "4. About" },
            { Z: "5. For" },
            { Z: "6. Out with" },
          ],
        },
      ],
      tablasTiempoP87: [
        {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "Z", label: "A", thClass: "colorLetraRojo" },
          ],
          items: [
            { Z: "1. What" },
            { Z: "2. Who" },
            { Z: "3. Where" },
            { Z: "4. How" },
            { Z: "5. When" },
            { Z: "6. What time" },
          ],
        },
        {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "Z", label: "B", thClass: "colorLetraRojo" },
          ],
          items: [
            { Z: "1. Are" },
            { Z: "2. Is" },
            { Z: "3. Do" },
            { Z: "4. Would" },
            { Z: "5. Will" },
            { Z: "6. Does" },
            { Z: "7. Can" },
            { Z: "8. Was" },
          ],
        },
        {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              label: "C",
              thClass: "colorLetraRojo",
            },
          ],
          items: [
            { Z: "1. It" },
            { Z: "2. You" },
            { Z: "3. She" },
            { Z: "4. We" },
            { Z: "5. I" },
            { Z: "6. That" },
            { Z: "7. Your" },
          ],
        },
        {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              label: "D",
              thClass: "colorLetraRojo",
            },
          ],
          items: [
            { Z: "1. Name" },
            { Z: "2. From" },
            { Z: "3. Have" },
            { Z: "4. Happened" },
            { Z: "5. Hungry" },
            { Z: "6. Going" },
            { Z: "7. Coming" },
            { Z: "8. Doing" },
            { Z: "9. Like" },
            { Z: "10. Shut" },
            { Z: "11. Mean" },
            { Z: "12. Going to" },
          ],
        },
        {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              label: "E",
              thClass: "colorLetraRojo",
            },
          ],
          items: [
            { Z: "1. Do now" },
            { Z: "2. To you" },
            { Z: "3. Something to drink" },
            { Z: "4. Day" },
            { Z: "5. Any money" },
            { Z: "6. Do for you" },
            { Z: "7. It" },
            { Z: "8. To go" },
          ],
        },
      ],
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