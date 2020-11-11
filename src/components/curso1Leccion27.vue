<template>
  <div>
    <div class="row">
      <h3 id="subTitulo">ORDINAL NUMBERS</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h3 style="text-align: justify">
          The abbreviation for ordinal numbers from the fourth is formed with the addition of "th" to the number. The dozens and units are separated by a hyphen from 20, e.g. 21
          st = twenty-first.
        </h3>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <listaIndex :tabla="$data.tablaP106" />
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h3 style="text-align: justify">
          Dates are expressed differently between America and other English-speaking countries. In America, they say
          the month first then the date (May 24 th). In the other English-speaking countries, they say the date first then the month (24
          th of May). Notice all other countries say “of”. The 24 th of May
        </h3>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <listaIndex :tabla="$data.tablaP106A" />
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">PRACTICE</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h5>Escribe la fecha de otro modo</h5>
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
        <h3 id="subTitulo">Listening section. write the month and the day.</h3>
    </div>
    <div class="row" v-for="(item, index) in preguntasCompletarP107.items">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <div :class="'col-sm-'+item.tamaño">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP107.nombre+index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
          />
        </div>
      </div>
    </div>

    <div class="row">
      <h3>MY SUPERMARKET MISADVENTURES</h3>
      <div class="col-sm-1">
        <h3>
          <strong>Vocabulary</strong>
        </h3>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <listaIndex :tabla="$data.tablaP107" />
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h3 style="text-align: justify">
          Today I had to go to the supermarket, to buy some things for my family. My mum had given me $15 to buy
          the weeks groceries. Included in the list was a half dozen apples, a dozen bananas, 750g of carrots, 500g of
          rice, six eggs, 3 litres of milk and a kilogram of chicken. I also had to buy a few other things to keep the
          kitchen cupboards full, like olive oil and a few more vegetables. Unfortunately, once I arrived in the supermarket, I realized the $15 was not going to be enough! The
          kilogram of chicken alone cost $6.95, the eggs cost 20 cents each and the milk cost $1.50 per litre. The most
          Logic of english Step 1
          VICTOR SIERRA ©
          expensive of all was the olive oil. My mum likes this expensive Spanish brand, and one litre cost another
          $6.49!
          Then, to make matters worse, as I was walking around the electronics section I slipped over and ended up
          breaking a $1,200 television!! When the store manager came over I tried to apologize, but he wanted me to
          pay for it. I told him I didn’t have the money, and he said I could pay for my groceries and come back later to
          pay for the television. However, when I told him I also didn’t have enough money for the groceries he
          looked absolutely furious!
          Now I’m walking home, and trying to figure out how to tell my mum that I need $1,200 to pay for a broken
          tv… I think she’s going to ground me for the next three years! Hopefully we can pay the money back in $50
          weekly payments over the next few months, but she will still be very angry either way.
          I need to go back to the supermarket, find the angry manager and pay for the groceries too… What a day!
        </h3>
      </div>
    </div>
    <div class="row">
      <h3 id="subTitulo">QUESTIONS</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6" id="text">
        <opcionMultiple
          :options="$data.cuestionarioP109"
          :rEsperadas="$data.respuestasCuestionarioP109"
          @respuestas="$data.mensajeRespuestasP109 = $event"
        />
      </div>
      <b-modal ref="my-modal109" hide-footer title="RESULTADO">{{mensajeRespuestasP109 }}</b-modal>
      <div class="col-sm-1"></div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-3">
        <b-button variant="primary" @click="showModal('my-modalP109')">VERIFICAR PREGUNTAS</b-button>
      </div>
    </div>
    <div class= "row">
      <div class= "col-sm-1"></div>
      <div class="col-sm-10">
        <b-card> 
        <h3 id="text-align: justify">
          Has terminado todas las lecciones del primer nivel, ahora estás en las capacidades de presentar el examen, has click en el botón para resolverlo.
        </h3>
          <div>
            <b-button style="margin: 10px;" size="lg" href="https://classroom.pikinglish.com/main/gradebook/index.php?cidReq=LOGIC1&id_session=0&gidReq=0&gradebook=0&origin=" variant="danger">HACER EXAMEN</b-button>
          </div>
        </b-card>
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
      mensajeRespuestasP109: "Complete las preguntas",
      respuestasCuestionarioP109: [
        "C",
        "A",
        "B",
        "C",
        "A",
        "B",
        "B",
        "A",
        "B",
        "B",
      ],
      cuestionarioP109: [
        {
          respuesta: "",
          pregunta: "1. How many pieces of fruit did the author need to buy?",
          options: [
            {
              text: "A) Six",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Twelve",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Eighteen",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "2. The author bought _______ eggs _______ apples",
          options: [
            {
              text: "A) The same amount of, as",
              value: "A",
              disabled: false,
            },
            {
              text: "B) more, than",
              value: "B",
              disabled: false,
            },
            {
              text: "C) less, than",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "3. How much did the author spend on eggs?",
          options: [
            {
              text: "A) One dollar",
              value: "A",
              disabled: false,
            },
            {
              text: "B) One hundred and twenty cents",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Twenty cents",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "4. How much did the author spend on milk?",
          options: [
            {
              text: "A) One dollar and fifty cents",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Three dollars",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Four dollars and fifty cents",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "5. What was the most expensive item the author bought?",
          options: [
            {
              text: "A) The olive oil.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) The chicken",
              value: "B",
              disabled: false,
            },
            {
              text: "C) The milk",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "6. How did the author break the television?",
          options: [
            {
              text: "A) He hit it with his groceries",
              value: "A",
              disabled: false,
            },
            {
              text: "B) He slipped",
              value: "B",
              disabled: false,
            },
            {
              text: "C) He walked into it",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "7. Why was the store manager so angry?",
          options: [
            {
              text: "A) Because the author couldn’t pay for the television",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Because the author couldn’t pay for the groceries",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Because the author couldn´t pay for the television or the groceries",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "8. “The author is worried he might be grounded”. What does this mean?",
          options: [
            {
              text: "A) He won’t be allowed to go out with his friends",
              value: "A",
              disabled: false,
            },
            {
              text: "B) He will have to work in the garden",
              value: "B",
              disabled: false,
            },
            {
              text: "C) He will have to work in the store to pay for the television",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "9. If the author can pay for the television by paying $50 a week, how many weeks will he need to pay back the $1,200?",
          options: [
            {
              text: "A) Twelve weeks",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Twenty-four weeks",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Thirty-six weeks",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "10. What word best describes the author’s day?",
          options: [
            {
              text: "A) Fun",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Stressful",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Boring",
              value: "C",
              disabled: false,
            },
          ],
        },
      ],
      preguntasCompletarP107: {
        nombre: "preguntasCompletarP105A",
        items: [
          {
            esperado: ["one hundred"],
            textoA: "1. School begins on",
            textoD: ".",
            tamaño: 5,
          },
          {
            esperado: ["ten"],
            textoA: "2. My sister will travel to France on",
            textoD: ".",
            tamaño: 8,
          },
          {
            esperado: ["ten"],
            textoA: "3. We will take the test on",
            textoD: ".",
            tamaño: 7,
          },
          {
            esperado: ["twelve"],
            textoA: "4. On",
            textoD: ", the store will have a big sale",
            tamaño: 8,
          },
          {
            esperado: ["Three hundred sixty four"],
            textoA: "5. Can you send me an email by",
            textoD: "?.",
            tamaño: 4,
          },
          {
            esperado: ["twenty four"],
            textoA: "6. You need to turn in your homework by",
            textoD: ".",
            tamaño: 5,
          },
          {
            esperado: ["one thousand four hundred forty"],
            textoA: "7. What time will your mom come on",
            textoD: "?.",
            tamaño: 6,
          },
          {
            esperado: ["sixty"],
            textoA: "8. The new students arrived on",
            textoD: ".",
            tamaño: 6,
          },
          {
            esperado: ["three thousand six hundred"],
            textoA: "9. My girlfriend and I went out for the first time on",
            textoD: ".",
            tamaño: 8,
          },
          {
            esperado: ["one thousand six hundred nine"],
            textoA: "10. I will return to my country on",
            textoD: ".",
            tamaño: 7,
          },
        ],
      },
      cuestionario1: {
        fields: [
          { key: "english", label: "AMERICAN DATE", thClass: "Yelow" },
          {
            key: "TRADUCCION_ESPAÑOL",
            label: "BRITISH DATE",
            thClass: "Yelow",
          },
        ],
        items: [
          {
            english: "On December 21 st 2012",
            TRADUCCION_ESPAÑOL: ["On the 21st of December, 2012"],
          },
          {
            english: "On July ninth 1984",
            TRADUCCION_ESPAÑOL: ["On the ninth of July 1984"],
          },
        ],
      },
      tablaP106: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "1", label: "1st First", thClass: "Green" },
          { key: "2", label: "2nd Second", thClass: "Green" },
          { key: "3", label: "3rd Third", thClass: "Green" },
          { key: "4", label: "4th fourth", thClass: "Green" },
          { key: "5", label: "5th Fifth", thClass: "Green" },
          { key: "6", label: "6th Sixth", thClass: "Green" },
          { key: "7", label: "7th Seventh", thClass: "Green" },
          { key: "8", label: "8th Eighth", thClass: "Green" },
          { key: "9", label: "9th ninth", thClass: "Green" },
          { key: "10", label: "10th tenth", thClass: "Green" },
        ],
        items: [
          {
            1: "11th Eleventh",
            2: "12th Twelfth",
            3: "13th Thirteenth",
            4: "14th fourteenth",
            5: "15th fifteenth",
            6: "16th Sixteenth",
            7: "17th seventeenth",
            8: "18th eighteenth",
            9: "19th nineteenth",
            10: "20th twentieth",
          },
          {
            1: "21st Twenty-first",
            2: "22nd Twenty-second",
            3: "23rd Twenty-third",
            4: "24th Twenty-fourth",
            5: "25th Twenty-fifth",
            6: "26th Twenty-sixth",
            7: "27th Twenty-seventh",
            8: "28th Twenty-eighth",
            9: "29th Twenty-ninth",
            10: "30th thirtieth",
          },
        ],
      },
      tablaP106A: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "1", label: "AMERICAN DATE", thClass: "Yelow" },
          { key: "2", label: "BRITISH DATE", thClass: "Yelow" },
        ],
        items: [
          {
            1: "Month- Day- Year",
            2: "Day- Month- Year",
          },
          {
            1: "On May 2nd, 2019",
            2: "On the 2nd of May, 2019",
          },
        ],
      },
      tablaP107: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "1", label: "English" },
          { key: "2", label: "Spanish" },
        ],
        items: [
          {
            1: "Dozen",
            2: "Docena",
          },
          {
            1: "Misadventures",
            2: "Misadventures",
          },
          {
            1: "Groceries",
            2: "Comestibles",
          },
          {
            1: "Few",
            2: "Pocos (as)",
          },
          {
            1: "To make matters worse",
            2: "Para empeorar las cosas",
          },
          {
            1: "Slip",
            2: "Deslizar9",
          },
          {
            1: "Apologize",
            2: "Disculpar",
          },
          {
            1: "Ground",
            2: "Que no permites salir de la casa",
          },
          {
            1: "Furious",
            2: "Furioso",
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