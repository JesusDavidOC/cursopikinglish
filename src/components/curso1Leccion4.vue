<template>
  <div>
    <div class="row" style="margin-top: -5em">
      <h3 id="subTitulo">MEZCLAS CON LAS FORMAS DEL VERBO</h3>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div
          class="col-sm-3"
          v-for="item in tablasTiempoP23"
          style="margin: 0; padding: 0"
        >
          <listaIndex :tabla="item" />
        </div>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">PRACTICE</h3>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" id="text">
        <i class="fa fa-diamond" style="font-size: 1.5em"></i>
        <a id="textPractice">Completar con la forma del verbo correcta</a>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <tablaTC :cuestionario="tablaP23" />
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" id="text">
        <i class="fa fa-diamond" style="font-size: 1.5em"></i>
        <a id="textPractice">
          <strong> Escribe el modificador correspondiente </strong>
          <a class="colorLetraRojo">DO-DOES-DID-WILL-WOULD</a>
        </a>
      </div>
    </div>

    <div class="row" v-for="(item, index) in preguntasCompletarP24.items">
      <b-col md="1"></b-col>
      <div class="col-md-11">
        <inputChecked
          :esperado="item.esperado"
          :name="preguntasCompletarP24.nombre + index"
          :conTexto="true"
          :textoA="item.textoA"
          :textoD="item.textoD"
          :tamano="item.tamano"
        />
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" id="text">
        <i class="fa fa-diamond" style="font-size: 1.5em"></i>
        <a id="textPractice">Marca la negacion correcta</a>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6">
        <opcionMultiple
          id="text"
          :options="$data.cuestionarioP24"
          :rEsperadas="$data.respuestasCuestionarioP24"
          @respuestas="$data.mensajeRespuestasP24 = $event"
        />
      </div>
      <b-modal ref="my-modalP18" hide-footer title="RESULTADO">{{
        mensajeRespuestasP24
      }}</b-modal>
      <div class="col-sm-1"></div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-3">
        <b-button variant="primary" @click="showModal('my-modalP18')"
          >VERIFICAR PREGUNTAS</b-button
        >
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">CONCLUIR USO DE LA LÓGICA A TRAVÉS DEL “2 4 5 12”</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <ul>
          <dt v-for="item in listaConclusionP25" class="fuenteDiamond">
            <i class="fa fa-diamond"></i>
            <a>{{ item }}</a>
          </dt>
        </ul>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">PRACTICE</h3>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" id="text">
        <i class="fa fa-diamond" style="font-size: 1.5em"></i>
        <a id="textPractice"
          >Ubica la forma correspondiente del verbo en las siguientes
          oraciones.</a
        >
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div
          class="col-sm-12"
          v-for="(item, index) in tablasP25"
          style="margin-bottom: 2em"
        >
          <tablaTC :cuestionario="item" />
        </div>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" id="text">
        <i class="fa fa-diamond" style="font-size: 1.5em"></i>
        <a id="textPractice"
          >Completa las siguientes oraciones con la forma correcta del verbo.</a
        >
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <b-row v-for="(item, index) in preguntasCompletarP26.items">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP26.nombre + index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
            :audio="item.audio"
            :tamano="item.tamano"
          />
        </b-row>
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
    opcionMultiple,
    listaIndex,
    inputChecked,
    posiblesRespuestasTabla,
    tablaTC,
  },
  data() {
    return {
      preguntasCompletarP26: {
        nombre: "preguntasCompletarP24",
        items: [
          {
            esperado: ["working"],
            textoA: "1.   I am",
            textoD: "<span class='colorLetraRojo'>(work-worked-worked-working)</span> - <strong>Estoy trabajando.</strong>",
            tamano: 47,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R1.mp3",
          },
          {
            esperado: ["go"],
            textoA: "2.   I don’t",
            textoD:
              "anywhere <span class='colorLetraRojo'>(go-went-gone-going)</span> - <strong>Yo no voy a ninguna parte.</strong>",
            tamano: 51,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R2.mp3",
          },
          {
            esperado: ["have"],
            textoA: "3.   She can´t ",
            textoD:
              "a boyfriend now <span class='colorLetraRojo'>(have-has-had-having)</span> - <strong>Ella no puede tener un novio ahora.</strong>",
            tamano: 64,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R3.mp3",
          },
          {
            esperado: ["seen"],
            textoA: "4.   I haven’t ",
            textoD:
              "Victor today <span class='colorLetraRojo'>(see-saw-seen-seeing)</span> - <strong>No he visto a Víctor hoy.</strong>",
            tamano: 54,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R4.mp3",
          },
          {
            esperado: ["saw"],
            textoA: "5.   She",
            textoD:
              "Victor yesterday <span class='colorLetraRojo'>(see-saw-seen-seeing)</span> - <strong>Ella vio a Víctor ayer.</strong>",
            tamano: 52,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R5.mp3",
          },
          {
            esperado: ["had"],
            textoA: "6.   We",
            textoD:
              "an excellent class <span class='colorLetraRojo'>(have-has-had-having)</span> - <strong>Tuvimos una excelente clase.?</strong>",
            tamano: 58,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R6.mp3",
          },
          {
            esperado: ["been"],
            textoA: "7.   How have you",
            textoD: "? <span class='colorLetraRojo'>(be- was- been- being)</span> - <strong>¿Como has estado?.</strong>",
            tamano: 49,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R7.mp3",
          },
          {
            esperado: ["working"],
            textoA: "8.   She is",
            textoD: "<span class='colorLetraRojo'>(work-worked-worked-working)</span> - <strong>Ella está trabajando.</strong>",
            tamano: 50,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R8.mp3",
          },
          {
            esperado: ["do"],
            textoA: "9.   What did you",
            textoD: "last night? <span class='colorLetraRojo'>(do-did-done-doing)</span> - <strong>¿Qué hiciste anoche?.</strong>",
            tamano: 52,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R9.mp3",
          },
          {
            esperado: ["ate"],
            textoA: "10. I",
            textoD:
              "breakfast early <span class='colorLetraRojo'>(eat-ate-eaten-eating)</span> - <strong>Yo desayuné temprano.</strong>",
            tamano: 50,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R10.mp3",
          },
          {
            esperado: ["eat"],
            textoA: "11. I",
            textoD:
              "breakfast early <span class='colorLetraRojo'>(eat-ate-eaten-eating)</span> - <strong>Yo desayuno temprano.</strong>",
            tamano: 50,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R11.mp3",
          },
          {
            esperado: ["doing"],
            textoA: "12. What were you",
            textoD:
              "last night? <span class='colorLetraRojo'>(do-did-done-doing)</span> - <strong>¿Qué estabas haciendo anoche?.</strong>",
            tamano: 62,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R12.mp3",
          },
          {
            esperado: ["done"],
            textoA: "13. Have you ever",
            textoD: "that? <span class='colorLetraRojo'>(do-did-done-doing)</span> - <strong>¿Alguna vez has hecho eso?.</strong>",
            tamano: 56,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R13.mp3",
          },
          {
            esperado: ["do"],
            textoA: "14. We shouldn’t",
            textoD:
              "that. <span class='colorLetraRojo'>(do-did-done-doing)</span> - <strong>Nosotros no deberíamos hacer eso.</strong>",
            tamano: 57,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R14.mp3",
          },
          {
            esperado: ["study"],
            textoA: "15. You must",
            textoD:
              "for the exam. <span class='colorLetraRojo'>(study-studied-studied-studying)</span> - <strong>Tú debes estudiar para el examen.</strong>",
            tamano: 68,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R15.mp3",
          },
          {
            esperado: ["raining"],
            textoA: "16. It is",
            textoD:
              "a lot. <span class='colorLetraRojo'>(rain-rained-rained-raining)</span> - <strong>Está lloviendo mucho.</strong>",
            tamano: 50,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R16.mp3",
          },
          {
            esperado: ["like"],
            textoA: "17. What would you",
            textoD:
              "to do? <span class='colorLetraRojo'>(like-liked-liked-liking)</span> - <strong>¿Qué te gustaría hacer?.</strong>",
            tamano: 55,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R17.mp3",
          },
          {
            esperado: ["do"],
            textoA: "18. I",
            textoD:
              "sports once in a while. <span class='colorLetraRojo'>(do-did-done-doing)</span> - <strong>Yo hago deportes de vez en cuando.</strong>",
            tamano: 61,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R18.mp3",
          },
          {
            esperado: ["do"],
            textoA: "19. What does your father",
            textoD: "? <span class='colorLetraRojo'>(do-did-done-doing)</span> - <strong>¿Qué hace tu padre?.</strong>",
            tamano: 52,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R19.mp3",
          },
          {
            esperado: ["do"],
            textoA: "20. What can I",
            textoD: "for you? <span class='colorLetraRojo'>(do-did-done-doing)</span> - <strong>¿Qué puedo hacer por ti?.</strong>",
            tamano: 52,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R20.mp3",
          },
          {
            esperado: ["done"],
            textoA: "21. I haven’t ",
            textoD: "anything yet. <span class='colorLetraRojo'>(do-did-done-doing)</span> - <strong>No he hecho nada aún.</strong>",
            tamano: 53,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R21.mp3",
          },
          {
            esperado: ["did"],
            textoA: "22. You ",
            textoD:
              "a good job. <span class='colorLetraRojo'>(do-did-done-doing)</span> - <strong>Tú hiciste un buen trabajo.</strong>",
            tamano: 50,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R22.mp3",
          },
          {
            esperado: ["worked"],
            textoA: "23. My father",
            textoD:
              "for a big company. <span class='colorLetraRojo'>(work-worked- working)</span> -  <strong>Mi padre trabajó para una gran compañía.</strong> ",
            tamano: 72,
            audio: "/cursos/curso1/leccion4/audios/page26/AC1P25R23.mp3",
          },
        ],
      },
      tablasP25: [
        {
          fields: [
            {
              key: "complejo1",
              label: "AUXILIARIES",
            },
            {
              key: "A",
              label: "4.1",
            },
            {
              key: "B",
              label: "4.2",
            },
            {
              key: "C",
              label: "4.3",
            },
            {
              key: "D",
              label: "4.4",
            },
          ],
          items: [
            {
              complejo1: {
                lista: ["Go"],
                textoA: "Do you",
                textoD: "to school?",
                tamano: 19,
                audio: "/cursos/curso1/leccion4/audios/page25/AC1P24R1.mp3",
              },
              A: "Go",
              B: "Went",
              C: "Gone",
              D: "Going",
            },
            {
              complejo1: {
                lista: ["Eat"],
                textoA: "Did you",
                textoD: "vegetables?",
                tamano: 21,
                audio: "/cursos/curso1/leccion4/audios/page25/AC1P24R2.mp3",
              },
              A: "Eat",
              B: "Ate",
              C: "Eaten",
              D: "Eating",
            },
            {
              complejo1: {
                lista: ["Like"],
                textoA: "Would you",
                textoD: "to live in Peru?",
                tamano: 25,
                audio: "/cursos/curso1/leccion4/audios/page25/AC1P24R3.mp3",
              },
              A: "Like",
              B: "Liked",
              C: "Liked",
              D: "Liking",
            },
            {
              complejo1: {
                lista: ["do"],
                textoA: "What will you",
                textoD: "tomorrow?",
                tamano: 23,
                audio: "/cursos/curso1/leccion4/audios/page25/AC1P24R4.mp3",
              },
              A: "Do",
              B: "Did",
              C: "Done",
              D: "Doing",
            },
            {
              complejo1: {
                lista: ["Live"],
                textoA: "Where does she",
                textoD: "?",
                tamano: 20,
                audio: "/cursos/curso1/leccion4/audios/page25/AC1P24R5.mp3",
              },
              A: "Live",
              B: "Lived",
              C: "Lived",
              D: "Living",
            },
          ],
        },
        {
          fields: [
            {
              key: "complejo1",
              label: "Past-affirmative",
            },
            {
              key: "A",
              label: "4.1",
            },
            {
              key: "B",
              label: "4.2",
            },
            {
              key: "C",
              label: "4.3",
            },
            {
              key: "D",
              label: "4.4",
            },
          ],
          items: [
            {
              complejo1: {
                lista: ["Had"],
                textoA: "I",
                textoD: "a sandwich for lunch",
                tamano: 22,
                audio: "/cursos/curso1/leccion4/audios/page25/AC1P24R6.mp3",
              },
              A: "Have",
              B: "Had",
              C: "Had",
              D: "Having",
            },
            {
              complejo1: {
                lista: ["Went"],
                textoA: "We ",
                textoD: "to see a movie last night",
                tamano: 26,
                audio: "/cursos/curso1/leccion4/audios/page25/AC1P24R7.mp3",
              },
              A: "Go",
              B: "Went",
              C: "Gone",
              D: "Going",
            },
            {
              complejo1: {
                lista: ["Studied"],
                textoA: "I",
                textoD: "at this university.",
                tamano: 22,
                audio: "/cursos/curso1/leccion4/audios/page25/AC1P24R8.mp3",
              },
              A: "Study",
              B: "Studied",
              C: "Studied",
              D: "Studying",
            },
          ],
        },
        {
          fields: [
            {
              key: "complejo1",
              label: "HAVE-HAS-HAD",
            },
            {
              key: "A",
              label: "4.1",
            },
            {
              key: "B",
              label: "4.2",
            },
            {
              key: "C",
              label: "4.3",
            },
            {
              key: "D",
              label: "4.4",
            },
          ],
          items: [
            {
              complejo1: {
                lista: ["Been"],
                textoA: "How have you ",
                textoD: "?",
                tamano: 20,
                audio: "/cursos/curso1/leccion4/audios/page25/AC1P24R9.mp3",
              },
              A: "Be",
              B: "Was",
              C: "Been",
              D: "Being",
            },
            {
              complejo1: {
                lista: ["Left"],
                textoA: "I had",
                textoD: "the party before that happened",
                tamano: 31,
                audio: "/cursos/curso1/leccion4/audios/page25/AC1P24R10.mp3",
              },
              A: "Leave",
              B: "Left",
              C: "Left",
              D: "Leaving",
            },
            {
              complejo1: {
                lista: ["Eaten"],
                textoA: "She hasn´t",
                textoD: "yet",
                tamano: 19,
                audio: "/cursos/curso1/leccion4/audios/page25/AC1P24R11.mp3",
              },
              A: "Eat",
              B: "Ate",
              C: "Eaten",
              D: "Eating",
            },
          ],
        },
        {
          fields: [
            {
              key: "complejo1",
              label: "IS-AM-ARE-WAS-WERE",
            },
            {
              key: "A",
              label: "4.1",
            },
            {
              key: "B",
              label: "4.2",
            },
            {
              key: "C",
              label: "4.3",
            },
            {
              key: "D",
              label: "4.4",
            },
          ],
          items: [
            {
              complejo1: {
                lista: ["Thinking"],
                textoA: "What are you",
                textoD: "about?",
                tamano: 24,
                audio: "/cursos/curso1/leccion4/audios/page25/AC1P24R12.mp3",
              },
              A: "Think",
              B: "Thought",
              C: "Thought",
              D: "Thinking",
            },
            {
              complejo1: {
                lista: ["Going"],
                textoA: "Where were you",
                textoD: "?",
                tamano: 21,
                audio: "/cursos/curso1/leccion4/audios/page25/AC1P24R13.mp3",
              },
              A: "Go",
              B: "Went",
              C: "Gone",
              D: "Going",
            },
            {
              complejo1: {
                lista: ["Making"],
                textoA: "I am",
                textoD: "my bed",
                tamano: 18,
                audio: "/cursos/curso1/leccion4/audios/page25/AC1P24R14.mp3",
              },
              A: "Make",
              B: "Made",
              C: "Made",
              D: "Making",
            },
            {
              complejo1: {
                lista: ["Paying"],
                textoA: "Sorry! I was not",
                textoD: "attention",
                tamano: 25,
                audio: "/cursos/curso1/leccion4/audios/page25/AC1P24R15.mp3",
              },
              A: "Pay",
              B: "Paid",
              C: "Paid",
              D: "Paying",
            },
          ],
        },
      ],
      listaConclusionP25: [
        "Siempre recuerda para que sirven los modificadores (auxiliares): Para preguntar o negar.",
        "Recuerda que un verbo se usa en pasado solo en afirmación.",
        "Los verbos con poderes se niegan solos, ellos no necesitan auxiliares.",
        "El participio de un verbo se usa después de los verbos con poderes HAVE, HAS Y HAD.",
        "Un verbo se usa en presente también después de un AUXILIAR, CAN, COULD, SHOULD o MUST.",
        "Siempre que uses IS, AM, ARE, WAS Y WERE, al verbo que sigue se le agrega ING (progresivo).",
        "Los verbos regulares no cambian su raíz en pasado, ni participio y solo se le agrega ed.",
      ],
      mensajeRespuestasP24: "Complete las preguntas",
      respuestasCuestionarioP24: ["B", "A", "A", "A"],
      cuestionarioP24: [
        {
          respuesta: "",
          pregunta: "1. I don´t play soccer anymore.",
          audio: "/cursos/curso1/leccion4/audios/page24/AC1P23R1.mp3",
          options: [
            {
              text: "A) Yo ya no jugué fútbol.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Yo ya no juego fútbol.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "2. I didn´t understand what you said.",
          audio: "/cursos/curso1/leccion4/audios/page24/AC1P23R2.mp3",
          options: [
            {
              text: "A) Yo no entendí lo que dijiste.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Yo no entendería lo que dijiste.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "3. I wouldn´t like to work on Sundays.",
          audio: "/cursos/curso1/leccion4/audios/page24/AC1P23R3.mp3",
          options: [
            {
              text: "A) No me gustaría trabajar los domingos .",
              value: "A",
              disabled: false,
            },
            {
              text: "B) No me gustará trabajar los domingos.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "4. She doesn´t eat meat",
          audio: "/cursos/curso1/leccion4/audios/page24/AC1P23R4.mp3",
          options: [
            {
              text: "A) Ella no come carne.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Ella no comió carne.",
              value: "B",
              disabled: false,
            },
          ],
        },
      ],
      preguntasCompletarP24: {
        nombre: "preguntasCompletarP24",
        items: [
          {
            esperado: ["do"],
            textoA: "1.   <strong>¿Cómo te sientes?</strong> - How",
            textoD: "you feel?",
            tamano: 31,
          },
          {
            esperado: ["does"],
            textoA: "2.   <strong>¿Dónde vive ella?</strong> - Where ",
            textoD: "she live?",
            tamano: 33,
          },
          {
            esperado: ["will"],
            textoA: "3.   <strong>¿Cuándo te irás?</strong> - When",
            textoD: "you go?",
            tamano: 31,
          },
          {
            esperado: ["do"],
            textoA: "4.   <strong>¿Qué quieres?</strong> - What ",
            textoD: "you want?",
            tamano: 30,
          },
          {
            esperado: ["would"],
            textoA: "5.   <strong>¿Qué te gustaría?</strong> - What ",
            textoD: "you like?",
            tamano: 33,
          },
          {
            esperado: ["did"],
            textoA: "6.   <strong>¿Cuándo llegaste?</strong> - When ",
            textoD: "you arrive?",
            tamano: 34,
          },
          {
            esperado: ["will"],
            textoA: "7.   <strong>¿Dónde iras?</strong> - Where",
            textoD: "you go?",
            tamano: 29,
          },
          {
            esperado: ["did"],
            textoA: "8.   <strong>¿Cómo lo hiciste?</strong> - How ",
            textoD: "you do it?",
            tamano: 32,
          },
          {
            esperado: ["would"],
            textoA:
              "9.   <strong>¿Cuánto tiempo te gustaría quedarte?</strong> - How long",
            textoD: "you like to stay??",
            tamano: 53,
          },
          {
            esperado: ["does"],
            textoA: "10.    <strong>¿Por qué ella te odia?</strong> Why",
            textoD: "she hate you?",
            tamano: 37,
          },
          {
            esperado: ["did"],
            textoA: "11.   <strong>¿Dónde la conociste?</strong> ",
            textoD: "you meet her?",
            tamano: 33,
          },
          {
            esperado: ["do"],
            textoA: "12.   <strong>¿Qué opinas?</strong> What ",
            textoD: "you think?",
            tamano: 29,
          },
          {
            esperado: ["will"],
            textoA: "13.   <strong>¿Cuándo será?</strong> When ",
            textoD: "it be?",
            tamano: 28,
          },
        ],
      },
      tablaP23: {
        fields: [
          {
            key: "SPANISH",
            thClass: "Yelow",
          },
          {
            key: "PRESENT",
            thClass: "Yelow",
          },
          {
            key: "PAST",
            thClass: "Yelow",
          },
          {
            key: "PARTICIPLE",
            thClass: "Yelow",
          },
          {
            key: "PROGRESSIVE",
            thClass: "Yelow",
          },
          {
            key: "complejo1",
            label: "ENGLISH",
            thClass: "Yelow",
          },
        ],
        items: [
          {
            SPANISH: "Llover",
            PRESENT: "Rain",
            PAST: "Rained",
            PARTICIPLE: "Rained",
            PROGRESSIVE: "Raining",
            complejo1: {
              lista: ["raining"],
              textoA: "It is",
              textoD: "",
              tamano: 12,
              audio: "/cursos/curso1/leccion4/audios/page23/AC1P22R1.mp3",
            },
          },
          {
            SPANISH: "Ir",
            PRESENT: "Go",
            PAST: "Went",
            PARTICIPLE: "Gone",
            PROGRESSIVE: "Going",
            complejo1: {
              lista: ["gone"],
              textoA: "He has",
              textoD: "to school",
              tamano: 18,
              audio: "/cursos/curso1/leccion4/audios/page23/AC1P22R2.mp3",
            },
          },
          {
            SPANISH: "Comer",
            PRESENT: "Eat",
            PAST: "Ate",
            PARTICIPLE: "Eaten",
            PROGRESSIVE: "Eating",
            complejo1: {
              lista: ["eating"],
              textoA: "What are you",
              textoD: "?",
              tamano: 18,
              audio: "/cursos/curso1/leccion4/audios/page23/AC1P22R3.mp3",
            },
          },
          {
            SPANISH: "Ver",
            PRESENT: "See",
            PAST: "Saw",
            PARTICIPLE: "Seen",
            PROGRESSIVE: "Seeing",
            complejo1: {
              lista: ["see"],
              textoA: "I can´t",
              textoD: "very well",
              tamano: 17,
              audio: "/cursos/curso1/leccion4/audios/page23/AC1P22R4.mp3",
            },
          },
          {
            SPANISH: "Ver",
            PRESENT: "See",
            PAST: "Saw",
            PARTICIPLE: "Seen",
            PROGRESSIVE: "Seeing",
            complejo1: {
              lista: ["seen"],
              textoA: "I have never",
              textoD: "that movie",
              tamano: 22,
              audio: "/cursos/curso1/leccion4/audios/page23/AC1P22R5.mp3",
            },
          },
          {
            SPANISH: "Encontrar",
            PRESENT: "Find",
            PAST: "Found",
            PARTICIPLE: "Found",
            PROGRESSIVE: "Finding",
            complejo1: {
              lista: ["found"],
              textoA: "I finally",
              textoD: "my wallet after 2 days",
              tamano: 26,
              audio: "/cursos/curso1/leccion4/audios/page23/AC1P22R6.mp3",
            },
          },
          {
            SPANISH: "Sentir",
            PRESENT: "Feel",
            PAST: "Felt",
            PARTICIPLE: "Felt",
            PROGRESSIVE: "Feeling",
            complejo1: {
              lista: ["feeling"],
              textoA: "I am",
              textoD: "on top of the world",
              tamano: 23,
              audio: "/cursos/curso1/leccion4/audios/page23/AC1P22R7.mp3",
            },
          },
          {
            SPANISH: "Comprar",
            PRESENT: "Buy",
            PAST: "Bought",
            PARTICIPLE: "Bought",
            PROGRESSIVE: "Buying",
            complejo1: {
              lista: ["buy"],
              textoA: "I must",
              textoD: "a present for Britney",
              tamano: 23,
              audio: "/cursos/curso1/leccion4/audios/page23/AC1P22R8.mp3",
            },
          },
          {
            SPANISH: "Tener",
            PRESENT: "Have",
            PAST: "Had",
            PARTICIPLE: "Had",
            PROGRESSIVE: "Having",
            complejo1: {
              lista: ["had"],
              textoA: "I had never",
              textoD: "a friend like you",
              tamano: 24,
              audio: "/cursos/curso1/leccion4/audios/page23/AC1P22R9.mp3 ",
            },
          },
          {
            SPANISH: "Dar",
            PRESENT: "Give",
            PAST: "Gave",
            PARTICIPLE: "Given",
            PROGRESSIVE: "Giving",
            complejo1: {
              lista: ["give"],
              textoA: "She didn´t",
              textoD: "me my wallet",
              tamano: 22,
              audio: "/cursos/curso1/leccion4/audios/page23/AC1P22R10.mp3",
            },
          },
          {
            SPANISH: "Olvidar",
            PRESENT: "Forget",
            PAST: "Forgot",
            PARTICIPLE: "Forgotten",
            PROGRESSIVE: "Forgetting",
            complejo1: {
              lista: ["forgotten"],
              textoA: "I have not",
              textoD: "you yet",
              tamano: 21,
              audio: "/cursos/curso1/leccion4/audios/page23/AC1P22R11.mp3",
            },
          },
          {
            SPANISH: "Decidir",
            PRESENT: "Decide",
            PAST: "Decided",
            PARTICIPLE: "Decided",
            PROGRESSIVE: "Deciding",
            complejo1: {
              lista: ["Decide"],
              textoA: "You should",
              textoD: "who to live with",
              tamano: 25,
              audio: "/cursos/curso1/leccion4/audios/page23/AC1P22R12.mp3",
            },
          },
          {
            SPANISH: "despertar",
            PRESENT: "Wake",
            PAST: "Woke",
            PARTICIPLE: "Woken",
            PROGRESSIVE: "Waking",
            complejo1: {
              lista: ["Waking"],
              textoA: "What time did you",
              textoD: "up today?",
              tamano: 26,
              audio: "/cursos/curso1/leccion4/audios/page23/AC1P22R13.mp3",
            },
          },
          {
            SPANISH: "Pensar",
            PRESENT: "Think",
            PAST: "Thought",
            PARTICIPLE: "Thought",
            PROGRESSIVE: "Thinking",
            complejo1: {
              lista: ["Thinking"],
              textoA: "I was",
              textoD: "about what you told me",
              tamano: 27,
              audio: "/cursos/curso1/leccion4/audios/page23/AC1P22R14.mp3",
            },
          },
          {
            SPANISH: "Conducir",
            PRESENT: "Drive",
            PAST: "Drove",
            PARTICIPLE: "Driven",
            PROGRESSIVE: "Driving",
            complejo1: {
              lista: ["Driven"],
              textoA: "She has never",
              textoD: "a car",
              tamano: 21,
              audio: "/cursos/curso1/leccion4/audios/page23/AC1P22R15.mp3",
            },
          },
          {
            SPANISH: "Aprender",
            PRESENT: "Learn",
            PAST: "Learned",
            PARTICIPLE: "Learned",
            PROGRESSIVE: "Learning",
            complejo1: {
              lista: ["Learn"],
              textoA: "You need to",
              textoD: "the numbers in English",
              tamano: 29,
              audio: "/cursos/curso1/leccion4/audios/page23/AC1P22R16.mp3",
            },
          },
        ],
      },
      tablasTiempoP23: [
        {
          bordered: false,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              label: "PRESENT",
              thClass: "colorLetraRojo",
            },
          ],
          items: [
            {
              Z: "Do",
            },
            {
              Z: "Does",
            },
            {
              Z: "Did",
            },
            {
              Z: "Will",
            },
            {
              Z: "Would",
            },
            {
              Z: "Can",
            },
            {
              Z: "Could",
            },
            {
              Z: "Should",
            },
            {
              Z: "Must",
            },
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
              label: "PAST",
              thClass: "colorLetraRojo",
            },
          ],
          items: [
            {
              Z: "Oraciones Afirmativas",
            },
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
              label: "PARTICIPLE " + "'ado-ido'",
              thClass: "colorLetraRojo",
            },
          ],
          items: [
            {
              Z: "Have",
            },
            {
              Z: "Has",
            },
            {
              Z: "Had",
            },
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
              label: "PROGRESSIVE \n 'ando-endo'",
              thClass: "colorLetraRojo",
            },
          ],
          items: [
            {
              Z: "Is",
            },
            {
              Z: "Am",
            },
            {
              Z: "Are",
            },
            {
              Z: "Was",
            },
            {
              Z: "Were",
            },
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

/deep/ .Blue {
  background-color: cornflowerblue;
}

/deep/ .Red {
  background-color: crimson;
}

/deep/ .Yelow {
  background-color: yellow;
}

/deep/ .Green {
  background-color: chartreuse;
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
  font-size: 2em;
  color: black;
  font-family: "PT Sans";
  font-weight: bold;
  margin-bottom: auto;
}

#numeroMagico2 {
  background: yellow;
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

#text,
#inputText {
  text-align: left;
  margin-left: 1em;
}

#textoCompromiso {
  text-align: left;
  margin-bottom: 1em;
  font-size: 1.5em;
}

#i {
  padding-right: 0;
  text-align: end;
}
</style>
