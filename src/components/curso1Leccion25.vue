<template>
  <div>
    <div class="row">
      <h3 id="titulo">PROCESO COMPLETADO CON ÉXITO SOBRE LA LÓGICA DEL INGLÉS</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h3 style="text-align: justify">
          El número mágico parte 1 es una recopilación de la gramática vista desde el punto lógico para diseñar
          oraciones y entender lecturas básicas.
        </h3>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-1" id="numeroMagico2">2</div>
      <div class="col-sm-3" id="campoTextoP11">
        <h2>Tipos de verbos:</h2>
      </div>
      <div class="col-sm-6" id="campoTextoP11">
        <h3 id="text">Regulares e Irregulares.</h3>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-1" id="numeroMagico4">4</div>
      <div class="col-sm-3" id="campoTextoP11">
        <h3>Formas de escribir un verbo:</h3>
      </div>
      <div class="col-sm-6" id="campoTextoP11">
        <h3 id="text">Presente, Pasado, Participio Y Progresivo.</h3>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-1" id="numeroMagico5">5</div>
      <div class="col-sm-3" id="campoTextoP11">
        <h2>Modificadores de tiempo:</h2>
      </div>
      <div class="col-sm-6" id="campoTextoP11">
        <h3 id="text">Do, Does, Did, Will y Would.</h3>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-1" id="numeroMagico12">12</div>
      <div class="col-sm-3" id="campoTextoP11">
        <h2>Verbos con súper poder:</h2>
      </div>
      <div class="col-sm-6" id="campoTextoP11">
        <h3 id="text">Have-Has-Had /Is-Am-Are-Was-Were/Can-Could-Should-Must</h3>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">NÚMERO MÁGICO PARTE 1</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h3
          style="text-align: justify"
        >En esta última sección del libro podrás practicar vocabulario con explicaciones lógicas.</h3>
        <h3>
          <ul style="text-align: left">
            <li>FAMILY MEMBERS</li>
            <li>MONTHS OF THE YEAR</li>
            <li>CARDINAL NUMBERS</li>
            <li>ORDINAL NUMBERS</li>
          </ul>
        </h3>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">FAMILY MEMBERS</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h3 class="colorLetraAzul">ROLES</h3>
        <listaIndex :tabla="$data.tablaP94" />
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h3 class="colorLetraAzul">IN-LAW</h3>
        <listaIndex :tabla="$data.tablaP94A" />
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h3 class="colorLetraAzul">STEP</h3>
        <listaIndex :tabla="$data.tablaP94B" />
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h3 class="colorLetraAzul">GRAND</h3>
        <listaIndex :tabla="$data.tablaP94C" />
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h5 class="colorLetraAzul">GOD</h5>
        <listaIndex :tabla="$data.tablaP94D" />
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h3 style="text-align: left">MY FAMILY TREE</h3>
        <h3 style="text-align: justify">
          My name is Victor Hugo Sierra, I have two brothers, one daughter and one godson; my brothers are Oscar and
          Julian and my daughter´s name is Karen, she is 14 and Elkin is my godson. My parents’ names are Alba and
          Hugo. Oscar, my second oldest brother has four sons; Cristian, Pablo, Julian and Samuel. Cristian and Pablo´s
          mother is Maryori and Julian and Samuel´s mother is Idaly. My grandparents on my mother’s side were Victor
          and Lucidia and on my father’s side were Fabio and Alicia. My mother Alba has two brothers and four sisters;
          Frederman, Alex, Mirian, Angela, Judith and Maria. My dad has five brothers and three sisters; Edgar, Fabio, Pedro, Orlando, Gentil, Fany, Farides and Fabiola. My uncles, Frederman and Gentil are dead. My mother’s
          siblings all have children. My aunt Mirian and Hermes have three sons and one daughter; Diego, Harol, Anderson and Lorena.
        </h3>
        <h3
          class="colorLetraAzul"
          style="font-style: italic; text-align: left"
        >Complete the following sentences according to the information above.</h3>
      </div>
    </div>
    <div class="row" v-for="(item, index) in preguntasCompletarP100.items">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <div :class="'col-sm-'+item.tamaño">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP100.nombre+index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
            :audio="item.audio"
          />
        </div>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h5 style="text-align: left">MY BIG COMPLICATED FAMILY</h5>
        <h5 style="text-align: justify">
          My name is Stephen and when I was a baby I was adopted by Mr and Mrs smith. The Smiths already had 1
          biological child named Laura and 2 adopted children, Melanie and Fred. Mr Smith has 2 brothers-Uncle Todd
          and Uncle Jack and 1 sister Aunty Meredith. Mrs Smith has 1 sister- Aunty Georgia. I love my adopted family
          very much and I consider them my real family. Until I was 19-years-old I didn’t know anything about my
          biological family or why I had been adopted. However, due to some surprising events I learned about my
          biological family sooner than I had expected. It all started when I was in my local bar and I locked eyes with a
          beautiful older woman. She was around 50-years-old with long, wavy red hair and a curvaceous body.
          Immediately, I felt a connection with her. That night we spent the whole night drinking beers and talking about
          life. She was the one! I went home to tell my family. Uncle Todd, my Dad and my Mum were all in the kitchen
          when I arrived home and I announced that I was in love with Miss Dorothy Perkins. There was silence in the
          kitchen. Dorothy Perkins was my biological father´s sister meaning she was my Aunty!!! Now, I had found and
          lost the love of my life in one day and I had met someone in my biological family. In the following days I met
          my biological Mum and Dad, Sara and Damien. They had 2 children years after I was adopted and so I met
          them too, by brothers David and Matthew. I´m 23 now and while I still have not found love I am thankful for
          my big and complicated family.
        </h5>
        <h5
          class="colorLetraAzul"
          style="font-style: italic; text-align: left"
        >Complete the following sentences according to the information above.</h5>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6" id="text">
        <opcionMultiple
          :options="$data.cuestionarioP101"
          :rEsperadas="$data.respuestasCuestionarioP101"
          @respuestas="$data.mensajeRespuestasP101 = $event"
        />
      </div>
      <b-modal ref="my-modalP101" hide-footer title="RESULTADO">{{mensajeRespuestasP101 }}</b-modal>
      <div class="col-sm-1"></div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-3">
        <b-button variant="primary" @click="showModal('my-modalP101')">VERIFICAR PREGUNTAS</b-button>
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
      mensajeRespuestasP101: "Complete las preguntas",
      respuestasCuestionarioP101: [
        "B",
        "B",
        "C",
        "B",
        "A",
        "B",
        "A",
        "C",
        "B",
        "A",
        "A",
      ],
      cuestionarioP101: [
        {
          respuesta: "",
          pregunta: "1. How old was Stephen when he was adopted?",
          options: [
            {
              text: "A) Baby",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Child",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Teenage",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "2. What was Stephen´s relationship to Mr and Mrs Smith?",
          options: [
            {
              text: "A) Biological parents",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Adoptive parents",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Grandparents",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "3. How old was Stephen when he met the curvaceous, red-headed woman?",
          options: [
            {
              text: "A) 23",
              value: "A",
              disabled: false,
            },
            {
              text: "B) 19",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Unknown",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "4. How was she related to him?",
          options: [
            {
              text: "A) Wife",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Aunty",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Mother",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "5. Where did they meet?",
          options: [
            {
              text: "A) In his kitchen",
              value: "A",
              disabled: false,
            },
            {
              text: "B) in the street",
              value: "B",
              disabled: false,
            },
            {
              text: "C) in a bar",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "6. How many sisters does Stephen have (adoptive and biological)?",
          options: [
            {
              text: "A) 3",
              value: "A",
              disabled: false,
            },
            {
              text: "B) 2",
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
          pregunta:
            "7. How many brothers does Stephen have (adoptive and biological)? ",
          options: [
            {
              text: "A) 3",
              value: "A",
              disabled: false,
            },
            {
              text: "B) 2",
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
          pregunta: "8. What is Sara´s relationship to Todd?",
          options: [
            {
              text: "A) Sister-in-law",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Friends",
              value: "B",
              disabled: false,
            },
            {
              text: "C) No relation",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "9. What is Meredith´s relationship to Mrs Smith?",
          options: [
            {
              text: "A) Sisters",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Step-sister",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Sister-in-law",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "10. How many children do Mr and Mrs Smith have?",
          options: [
            {
              text: "A) 3",
              value: "A",
              disabled: false,
            },
            {
              text: "B) 2",
              value: "B",
              disabled: false,
            },
            {
              text: "C) That one",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "11. What is Laura´s relationship to Meredith?",
          options: [
            {
              text: "A) Adoptive Aunt",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Sister-in-law",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Aunt",
              value: "C",
              disabled: false,
            },
          ],
        },
      ],
      preguntasCompletarP100: {
        nombre: "preguntasCompletarP24",
        items: [
          {
            esperado: ["two"],
            textoA: "1.  Victor has",
            textoD: "brothers.",
            tamaño: 4,
            audio:
              "https://classroom.pikinglish.com/cursos/curso1/leccion25/audios/page%20100/AC1P100R2q1.mp3",
          },
          {
            esperado: ["sister"],
            textoA: "2. Mirian is Alba´s ",
            textoD: "",
            tamaño: 4,
            audio:
              "https://classroom.pikinglish.com/cursos/curso1/leccion25/audios/page%20100/AC1P100R3q2.mp3",
          },
          {
            esperado: ["niece"],
            textoA: "3. Karen is Oscar´s",
            textoD: "",
            tamaño: 4,
            audio:
              "https://classroom.pikinglish.com/cursos/curso1/leccion25/audios/page%20100/AC1P100R4q3.mp3",
          },
          {
            esperado: ["parents in law"],
            textoA: "4. Alba´s",
            textoD: "are Fabio and Alicia",
            tamaño: 5,
            audio:
              "https://classroom.pikinglish.com/cursos/curso1/leccion25/audios/page%20100/AC1P100R5q4.mp3",
          },
          {
            esperado: ["uncle"],
            textoA: "5. Oscar is Karen´s",
            textoD: "",
            tamaño: 4,
            audio:
              "https://classroom.pikinglish.com/cursos/curso1/leccion25/audios/page%20100/AC1P100R6q5.mp3",
          },
          {
            esperado: ["three sons"],
            textoA: "6. Mirian has",
            textoD: "and one daughter",
            tamaño: 6,
            audio:
              "https://classroom.pikinglish.com/cursos/curso1/leccion25/audios/page%20100/AC1P100R7q6.mp3",
          },
          {
            esperado: ["grandmother"],
            textoA: "7. Alba is Christian´s",
            textoD: "",
            tamaño: 5,
            audio:
              "https://classroom.pikinglish.com/cursos/curso1/leccion25/audios/page%20100/AC1P100R8q7.mp3",
          },
          {
            esperado: ["brother"],
            textoA: "8. Oscar is Victor´s",
            textoD: "",
            tamaño: 5,
            audio:
              "https://classroom.pikinglish.com/cursos/curso1/leccion25/audios/page%20100/AC1P100R9q8.mp3",
          },
          {
            esperado: ["daughter"],
            textoA: "9. Karen is Victor´s",
            textoD: "",
            tamaño: 5,
            audio:
              "https://classroom.pikinglish.com/cursos/curso1/leccion25/audios/page%20100/AC1P100R10q9.mp3",
          },
          {
            esperado: ["cousin"],
            textoA: "10. Lorena is Victor´s",
            textoD: "",
            tamaño: 5,
            audio:
              "https://classroom.pikinglish.com/cursos/curso1/leccion25/audios/page%20100/AC1P100R11q10.mp3",
          },
          {
            esperado: ["sister in law"],
            textoA: "11. Idaly is Victor´s",
            textoD: "",
            tamaño: 5,
            audio:
              "https://classroom.pikinglish.com/cursos/curso1/leccion25/audios/page%20100/AC1P100R12q11.mp3",
          },
          {
            esperado: ["husband"],
            textoA: "12. Hermes is Mirian´s",
            textoD: "",
            tamaño: 5,
            audio:
              "https://classroom.pikinglish.com/cursos/curso1/leccion25/audios/page%20100/AC1P100R13q12.mp3",
          },
          {
            esperado: ["godfather"],
            textoA: "13. Victor is Elkin´s",
            textoD: "",
            tamaño: 5,
            audio:
              "https://classroom.pikinglish.com/cursos/curso1/leccion25/audios/page%20100/AC1P100R14q13.mp3",
          },
          {
            esperado: ["grandparents"],
            textoA: "13. Fabio and Alicia are Victor´s",
            textoD: "",
            tamaño: 6,
            audio:
              "https://classroom.pikinglish.com/cursos/curso1/leccion25/audios/page%20100/AC1P100R15q14.mp3",
          },
        ],
      },
      tablaP94: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "1", label: "Mother" },
          { key: "2", label: "Madre" },
          { key: "3", label: "Nephew" },
          { key: "4", label: "Sobrino" },
          { key: "5", label: "Widow" },
          { key: "6", label: "Viuda" },
        ],
        items: [
          {
            1: "Father",
            2: "Padre",
            3: "Niece",
            4: "Sobrina",
            5: "Widower",
            6: "Viudo",
          },
          {
            1: "Brother",
            2: "Hermano",
            3: "Husband",
            4: "Esposo",
            5: "Housewife",
            6: "Ama de casa",
          },
          {
            1: "Sister",
            2: "Hermana",
            3: "Wife",
            4: "Esposa",
            5: "Housekeeper-maid",
            6: "Empleada",
          },
          {
            1: "Son",
            2: "Hijo",
            3: "Boyfriend",
            4: "Novio",
            5: "Soulmate",
            6: "Alma gemela",
          },
          {
            1: "Daughter",
            2: "Hija",
            3: "Girlfriend",
            4: "Novia",
            5: "Neighbor",
            6: "Vecino",
          },
          {
            1: "Uncle",
            2: "Tio",
            3: "Couple",
            4: "Novios, pareja",
            5: "Loved one",
            6: "Ser querido",
          },
          {
            1: "Aunt",
            2: "Tia",
            3: "Significant other",
            4: "Pareja (Informal)",
            5: "Friend",
            6: "Amigo",
          },
          {
            1: "Cousin",
            2: "Primo (a)",
            3: "Relatives",
            4: "Familiar",
            5: "Acquaintance",
            6: "Conocido",
          },
        ],
      },
      tablaP94A: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "1", label: "Mother-in-law" },
          { key: "2", label: "Suegra" },
        ],
        items: [
          {
            1: "Father-in-law",
            2: "Suegro",
          },
          {
            1: "Son-in-law",
            2: "Yerno",
          },
          {
            1: "Daughter-in-law",
            2: "Nuera",
          },
          {
            1: "Bother-in-law",
            2: "Cuñado",
          },
          {
            1: "Sister-in-law",
            2: "Cuñada",
          },
          {
            1: "Parents-in-law",
            2: "Suegros",
          },
        ],
      },
      tablaP94B: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "1", label: "Stepmother" },
          { key: "2", label: "Madrastra" },
        ],
        items: [
          {
            1: "Stepfather",
            2: "Padrastro",
          },
          {
            1: "Stepson",
            2: "Hijastro",
          },
          {
            1: "Stepdaughter",
            2: "Hijastra",
          },
          {
            1: "Stepbrother",
            2: "Hermanastro",
          },
          {
            1: "Stepsister",
            2: "Hermanastra",
          },
        ],
      },
      tablaP94C: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "1", label: "Grandparents" },
          { key: "2", label: "Abuelos" },
        ],
        items: [
          {
            1: "Grandmother",
            2: "Abuela",
          },
          {
            1: "Grandma",
            2: "Abue",
          },
          {
            1: "Granddaddy",
            2: "Abuelito",
          },
          {
            1: "Grandfather",
            2: "Abuelo",
          },
          {
            1: "Grandson",
            2: "Nieto",
          },
          {
            1: "Granddaughter",
            2: "Nieta",
          },
        ],
      },
      tablaP94D: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "1", label: "Godfather" },
          { key: "2", label: "Padrino" },
        ],
        items: [
          {
            1: "Godmother",
            2: "Madrina",
          },
          {
            1: "Godson",
            2: "Ahijado",
          },
          {
            1: "Goddaughter",
            2: "Ahijada",
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
/deep/.colorLetraAzul {
  color: blue;
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