//<template>
  <div>
    <div>

      <div class="row">
        <div class="col-sm-12">
          <h3 id="subTitulo">READING COMPREHENSION</h3>
        </div>
      </div>

      <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-6" id="text">
          <opcionMultiple
            :options="$data.cuestionarioP13"
            :rEsperadas="$data.respuestasCuestionarioP13"
            @respuestas="mensajeRespuestasP13 = $event"
          />
        </div>
        <b-modal ref="my-modal1" hide-footer title="RESULTADO">{{
          mensajeRespuestasP13
        }}</b-modal>
        <div class="col-sm-1"></div>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-3">
        <b-button variant="primary" @click="showModal('my-modal1')"
          >VERIFICAR PREGUNTAS</b-button
        >
      </div>
    </div>
    <br>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-7" style="text-align:left;">
        <a id="textPractice">
          Escribe las oraciones del dialogo frente a cada verbo en presente.
        </a>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <tablaTC
          :cuestionario="$data.tablaA"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <div class="col-sm-1"></div>
    </div>
    
    <div class="row">
      <div class="col-sm">
          <h3 id="subTitulo">LIST OF IRREGULAR VERBS</h3>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <listaIndex :tabla="$data.tablaP21" />
      </div>
    </div>

  </div>
</template>

<script>
import listaIndex from "./listaIndex";
import opcionMultiple from "./opcionMultiple";
import inputChecked from "./inputChecked";
import tablaTC from "./tablaTraduccionCodigos";

export default {
  components: {
    listaIndex,
    tablaTC,
    opcionMultiple,
    inputChecked,
  },
    methods: {
    showModal(text) {
      this.$refs[text].show();
    },
  },
  data() {
    return {
    
    tablaP21: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "Nro", label: "Rank", thClass: "Red" },
          { key: "bForm", label: "Base Form", thClass: "Red" },
          { key: "ptForm", label: "Past Tense Form", thClass: "Red" },
          { key: "pPartiple", label: "Past Participle",thClass: "Red"},
        ],
        items: [
          {
            Nro: "1",
            bForm: "Say(decir)",
            ptForm: "Said",
            pPartiple: "Said",
          },
          {
            Nro: "2",
            bForm: "Make (hacer)",
            ptForm: "Made",
            pPartiple: "Made",
          },
          {
            Nro: "3",
            bForm: "Go (ir)",
            ptForm: "Went",
            pPartiple: "Gone",
          },
          {
            Nro: "4",
            bForm: "Take (llevar-tomar)",
            ptForm: "Took",
            pPartiple: "Taken",
          },
          {
            Nro: "5",
            bForm: "Come (venir)",
            ptForm: "Came",
            pPartiple: "Come",
          },
          {
            Nro: "6",
            bForm: "See (ver)",
            ptForm: "Saw",
            pPartiple: "Seen",
          },
          {
            Nro: "7",
            bForm: "Know (saber)",
            ptForm: "Knew",
            pPartiple: "Known",
          },
          {
            Nro: "8",
            bForm: "Get (obtener)",
            ptForm: "Got",
            pPartiple: "got/gotten (US)",
          },
          {
            Nro: "9",
            bForm: "Give (dar)",
            ptForm: "Gave",
            pPartiple: "Given",
          },
          {
            Nro: "10",
            bForm: "Find (encontrar)",
            ptForm: "Found",
            pPartiple: "Found",
          },
          {
            Nro: "11",
            bForm: "Think (pensar)",
            ptForm: "Thought",
            pPartiple: "Thought",
          },
          {
            Nro: "12",
            bForm: "Tell (decir)",
            ptForm: "Told",
            pPartiple: "Told",
          },
          {
            Nro: "13",
            bForm: "Become (volverse)",
            ptForm: "Became",
            pPartiple: "Become",
          },
          {
            Nro: "14",
            bForm: "Show (mostrar)",
            ptForm: "Showed",
            pPartiple: "Shown",
          },
          {
            Nro: "15",
            bForm: "Leave (dejar,irse)",
            ptForm: "Left",
            pPartiple: "Left",
          },
          {
            Nro: "16",
            bForm: "Feel (sentir)",
            ptForm: "Felt",
            pPartiple: "Felt",
          },
          {
            Nro: "17",
            bForm: "Put (poner)",
            ptForm: "Put",
            pPartiple: "Put",
          },
          {
            Nro: "18",
            bForm: "Bring (traer)",
            ptForm: "Brought",
            pPartiple: "Brought",
          },
          {
            Nro: "19",
            bForm: "Begin (iniciar)",
            ptForm: "Began",
            pPartiple: "Begun",
          },
          {
            Nro: "20",
            bForm: "Keep (mantener)",
            ptForm: "Kept",
            pPartiple: "Kept",
          },
          {
            Nro: "21",
            bForm: "Hold (sostener)",
            ptForm: "Held",
            pPartiple: "Held",
          },
          {
            Nro: "22",
            bForm: "Write (escribir)",
            ptForm: "Wrote",
            pPartiple: "Written",
          },
          {
            Nro: "23",
            bForm: "Stand (pararse)",
            ptForm: "Stood",
            pPartiple: "Stood",
          },
          {
            Nro: "24",
            bForm: "Hear (oir)",
            ptForm: "Heard",
            pPartiple: "Heard",
          },
          {
            Nro: "25",
            bForm: "Let (permitir-dejar)",
            ptForm: "Let",
            pPartiple: "Let",
          },
          {
            Nro: "26",
            bForm: "Mean (significar-querer decir)",
            ptForm: "Meant",
            pPartiple: "Meant",
          },
          {
            Nro: "27",
            bForm: "Set (configurar)",
            ptForm: "Set",
            pPartiple: "Set",
          },
          {
            Nro: "28",
            bForm: "Meet (conocer-reunirse)",
            ptForm: "Met",
            pPartiple: "Met",
          },
          {
            Nro: "29",
            bForm: "Run (correr)",
            ptForm: "Ran",
            pPartiple: "Run",
          },
          {
            Nro: "30",
            bForm: "Pay (pagar)",
            ptForm: "Paid",
            pPartiple: "Paid",
          },
          {
            Nro: "31",
            bForm: "Sit (sentarse)",
            ptForm: "Sat",
            pPartiple: "Sat",
          },
          {
            Nro: "32",
            bForm: "Speak (hablar)",
            ptForm: "Spoke",
            pPartiple: "Spoken",
          },
          {
            Nro: "33",
            bForm: "Lie (mentir)",
            ptForm: "Lay",
            pPartiple: "Lain",
          },
          {
            Nro: "34",
            bForm: "Lead (dirigir)",
            ptForm: "Led",
            pPartiple: "Led",
          },
          {
            Nro: "35",
            bForm: "Read (leer)",
            ptForm: "Read",
            pPartiple: "Read",
          },
          {
            Nro: "36",
            bForm: "Grow (crecer-plantar)",
            ptForm: "Grew",
            pPartiple: "Grown",
          },
          {
            Nro: "37",
            bForm: "Lose (perder)",
            ptForm: "Lost",
            pPartiple: "Lost",
          },
          {
            Nro: "38",
            bForm: "Fall (caerse)",
            ptForm: "Fell",
            pPartiple: "Fallen",
          },
          {
            Nro: "39",
            bForm: "Send (enviar)",
            ptForm: "Sent",
            pPartiple: "Sent",
          },
          {
            Nro: "40",
            bForm: "Build (construir)",
            ptForm: "Built",
            pPartiple: "Built",
          },
          {
            Nro: "41",
            bForm: "Understand (entender)",
            ptForm: "Understood",
            pPartiple: "Understood",
          },
          {
            Nro: "42",
            bForm: "Draw (dibujar)",
            ptForm: "Drew",
            pPartiple: "Drawn",
          },
          {
            Nro: "43",
            bForm: "Break (romper)",
            ptForm: "Broke",
            pPartiple: "Broken",
          },
          {
            Nro: "44",
            bForm: "Spend (gastar)",
            ptForm: "Spent",
            pPartiple: "Spent",
          },
          {
            Nro: "45",
            bForm: "Cut (cortar)",
            ptForm: "Cut",
            pPartiple: "Cut",
          },
          {
            Nro: "46",
            bForm: "Rise (levantar)",
            ptForm: "Rose",
            pPartiple: "Risen",
          },
          {
            Nro: "47",
            bForm: "Drive (conducir)",
            ptForm: "Drove",
            pPartiple: "Driven",
          },
          {
            Nro: "48",
            bForm: "Buy (comprar)",
            ptForm: "Bought",
            pPartiple: "Bought  ",
          },
          {
            Nro: "49",
            bForm: "Wear (ponerse)",
            ptForm: "Wore",
            pPartiple: "Worn",
          },
          {
            Nro: "50",
            bForm: "Choose (elegir)",
            ptForm: "Chose",
            pPartiple: "Chosen",
          },

        ],
      },

      cuestionarioP13: [
        {
          respuesta: "",
          pregunta: "1. What did David buy for lunch?",
          options: [
            {
              text: "A) A sandwish",
              value: "A",
              disabled: false,
            },
            {
              text: "B) a hamburger",
              value: "B",
              disabled: false,
            },
            {
              text: "C) a hamburger and a portion of frensh fries",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "2. How long did it take Ariel to get to the school from his home?",
          options: [
            {
              text: "A) 20 minutes",
              value: "A",
              disabled: false,
            },
            {
              text: "B) 10 minutes",
              value: "B",
              disabled: false,
            },
            {
              text: "C) 30 minutes",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "3. What did David see at one side of the road?",
          options: [
            {
              text: "A) His teacher",
              value: "A",
              disabled: false,
            },
            {
              text: "B) an accident",
              value: "B",
              disabled: false,
            },
            {
              text: "C) a black car",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "4. What time did Ariel have breakfast?",
          options: [
            {
              text: "A) At 8:00",
              value: "A",
              disabled: false,
            },
            {
              text: "B) at 7:00",
              value: "B",
              disabled: false,
            },
            {
              text: "C) at 9:00",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "5. What did Ariel ́s mother forget to pay?",
          options: [
            {
              text: "A) The milk",
              value: "A",
              disabled: false,
            },
            {
              text: "B) the electricity Bill",
              value: "B",
              disabled: false,
            },
            {
              text: "C) the water Bill",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "6 Who did David play basketball with?",
          options: [
            {
              text: "A) His teacher",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Victor",
              value: "B",
              disabled: false,
            },
            {
              text: "C) his mother",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "7. What time did Ariel get to school?",
          options: [
            {
              text: "A) At 8:00",
              value: "A",
              disabled: false,
            },
            {
              text: "B) at 7:20",
              value: "B",
              disabled: false,
            },
            {
              text: "C) at 7:00",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "8. What did David do at night before going to bed?",
          options: [
            {
              text: "A) He watched tv",
              value: "A",
              disabled: false,
            },
            {
              text: "B) He played basketball",
              value: "B",
              disabled: false,
            },
            {
              text: "C) He just drank orange juice",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "9.Did David take a quick shower?",
          options: [
            {
              text: "A) Yes, he did",
              value: "A",
              disabled: false,
            },
            {
              text: "B) no, he didn ́t",
              value: "B",
              disabled: false,
            },
          ],
        },
      ],

      mensajeRespuestasP13: "",
      respuestasCuestionarioP13: ["C", "A", "B", "B", "B", "B", "A", "C", "A"],

      tablaA: {
        fields: [
          { key: "PRESENT" },
          { key: "TRANSLATION" },
          { key: "complejo1", label: "PAST" },
          { key: "SPANISH" },
        ],
        items: [
          {
            PRESENT: "Have",
            TRANSLATION: "Tener",
            complejo1: { lista: ["I had a busy day"], audio: "https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R1%20Ihadabusyday.mp3" },
            SPANISH: "Tuve un dia  ocupado",
          },
          {
            PRESENT: "Have",
            TRANSLATION: "Tener",
            complejo1: { lista: ["I had a long day"] , audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R2%20ihadalongday.mp3"},
            SPANISH: "Tuve un dia  muy largo",
          },
          {
            PRESENT: "Wake",
            TRANSLATION: "Despertar",
            complejo1: { lista: ["I woke up very early"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R3%20iwokeupveryearly.mp3" },
            SPANISH: "Me desperté muy temprano",
          },
          {
            PRESENT: "Make",
            TRANSLATION: "Hacer",
            complejo1: { lista: ["My father made too much"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R4%20myfathermadetoomuch.mp3" },
            SPANISH: "Mi padre hizo mucho ruido",
          },
          {
            PRESENT: "Have",
            TRANSLATION: "Tener",
            complejo1: { lista: ["I had to take a shower with colder water"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R5%20ihadtotakeashower...mp3" },
            SPANISH: "Tuve que ducharme con agua fría",
          },
          {
            PRESENT: "Forget",
            TRANSLATION: "Olvidar",
            complejo1: {
              lista: ["My mother forgot to pay the electricity bill"], audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R6mymotherforgottopay...mp3"
            },
            SPANISH: "Mi madre olvido pagar la cuenta de electricidad",
          },
          {
            PRESENT: "Feel",
            TRANSLATION: "Sentir",
            complejo1: { lista: ["I felt very good"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R7ifeltverygood.mp3" },
            SPANISH: "Me senti muy bien",
          },
          {
            PRESENT: "Sit",
            TRANSLATION: "Sentarse",
            complejo1: { lista: ["Everyone including me sat at the table"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R8everyoneincludingme....mp3" },
            SPANISH: "Todos incluyendome nos sentamos a la mesa",
          },
          {
            PRESENT: "Eat",
            TRANSLATION: "Comer",
            complejo1: { lista: ["I ate faster than my sister"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R9iatefasterthanmysister.mp3" },
            SPANISH: "Comi mas rapido que mi hermana",
          },
          {
            PRESENT: "Have",
            TRANSLATION: "Tener",
            complejo1: { lista: ["I had to do the dishes"], audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R10ihadtodothedished.mp3" },
            SPANISH: "Tuve que lavar los platos",
          },
          {
            PRESENT: "Win",
            TRANSLATION: "Ganar",
            complejo1: { lista: ["Because i won"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R11becauseiwon.mp3" },
            SPANISH: "Porque yo gané",
          },
          {
            PRESENT: "Leave",
            TRANSLATION: "Dejar/Salir",
            complejo1: { lista: ["I left home "],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R12ilefthome.mp3" },
            SPANISH: "Salí de casa",
          },
          {
            PRESENT: "Get",
            TRANSLATION: "Llegar",
            complejo1: { lista: ["I got to school"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R13igottoschool.mp3" },
            SPANISH: "Llegué al colegio",
          },
          {
            PRESENT: "Get up",
            TRANSLATION: "Levantarse",
            complejo1: { lista: ["I woke up right away"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R14iwokeuprightaway.mp3" },
            SPANISH: "Me levanté enseguida",
          },
          {
            PRESENT: "Speak",
            TRANSLATION: "Hablar",
            complejo1: { lista: ["I spoke to the teacher"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R15ispoketotheteacher.mp3" },
            SPANISH: "Hablé con el profesor",
          },
          {
            PRESENT: "Wake",
            TRANSLATION: "Despertarse",
            complejo1: { lista: ["I woke up late"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R16iwokeuplate.mp3" },
            SPANISH: "Me desperté tarde",
          },
          {
            PRESENT: "Teach",
            TRANSLATION: "Enseñar",
            complejo1: { lista: ["I taught him"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R17itaughthim.mp3" },
            SPANISH: "Le enseñé a el",
          },
          {
            PRESENT: "Go",
            TRANSLATION: "Ir",
            complejo1: { lista: ["I went down the stairs"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R18iwentdownthestairs.mp3" },
            SPANISH: "Bajé las escaleras",
          },
          {
            PRESENT: "Tell",
            TRANSLATION: "Decir",
            complejo1: { lista: ["I told my mother"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R19itoldmymother.mp3" },
            SPANISH: "Le dije a mi madre",
          },
          {
            PRESENT: "Sit",
            TRANSLATION: "Sentarse",
            complejo1: { lista: ["We sat at the table"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R20wesatatthetable.mp3" },
            SPANISH: "Nos sentamos a la mesa",
          },
          {
            PRESENT: "Buy",
            TRANSLATION: "Comprar",
            complejo1: { lista: ["I bought a hamburger"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R21iboughtahamburger.mp3" },
            SPANISH: "Compré una hamburguesa",
          },
          {
            PRESENT: "Do",
            TRANSLATION: "Hacer",
            complejo1: { lista: ["I did the dishes"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R22ididthedishes.mp3" },
            SPANISH: "Hice los platos",
          },
          {
            PRESENT: "Could",
            TRANSLATION: "Pude",
            complejo1: { lista: ["I could take the bus"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R23icouldtakethebus.mp3" },
            SPANISH: "Pude tomar el  bus",
          },
          {
            PRESENT: "Give",
            TRANSLATION: "Dar",
            complejo1: { lista: ["I gave my mother a kiss"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R24igavemymotherakiss.mp3" },
            SPANISH: "Le di a mi madre un beso",
          },
          {
            PRESENT: "Leave",
            TRANSLATION: "Salir/Dejar",
            complejo1: { lista: ["I left home early"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R25ilefthomeearly.mp3" },
            SPANISH: "Salí de casa temprano",
          },
          {
            PRESENT: "See",
            TRANSLATION: "Ver",
            complejo1: { lista: ["I saw an accident"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R26isawanaccident.mp3" },
            SPANISH: "Vi un accidente",
          },
          {
            PRESENT: "Hit",
            TRANSLATION: "Golpear",
            complejo1: { lista: ["a car hit another car"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R27acarhitanothercar.mp3" },
            SPANISH: "Un carro golpeó otro carro",
          },
          {
            PRESENT: "Drink",
            TRANSLATION: "Beber",
            complejo1: { lista: ["I drank orange juice"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion14/audio/page%2057/AC1P57R28idrankorangejuice.mp3" },
            SPANISH: "Tomé jugo de naranja",
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
