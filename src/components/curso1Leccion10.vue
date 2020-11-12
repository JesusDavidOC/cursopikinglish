<template>
  <div>
     <div class="row">
      <i class="fa fa-diamond marginn-left" style="font-size: 1.5em"></i>

      <p class="parrafoBlack marginn-left">
        &nbsp;
        <b>CHOOSE, ORGANICE AND ADD THE RIGHT AUX.</b>
      </p>
      <br />
    </div>
    <div class="row">
        <div class="col-sm-1"></div>
        <div class="col-sm-6">
            <opcionMultiple id="text" :options="$data.cuestionarioP44" :rEsperadas="$data.respuestasCuestionarioP44" @respuestas="$data.mensajeRespuestasP44 = $event" />
        </div>
        <b-modal ref="my-modalP18" hide-footer title="RESULTADO">{{mensajeRespuestasP24 }}</b-modal>
        <div class="col-sm-1"></div>
    </div>
   
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-9 ">
        <div
          v-for="(item, index) in frases1Pag44"
          :class="' row col-sm-'+item.tamano"
          style="margin-bottom: 0.5em"
        >
          <div v-if="item.name == 'ice'"><inputCE :object="item" /></div>
          <div v-else-if="item.name == 'ic'">
            <inputChecked
              :resuelto="false"
              style="margin-right: 10px; display: inline-flex"
              :esperado="item.lista1"
              :conTexto="true"
              :textoA="item.textoA"
              :textoD="item.textoD"
            />
          </div>
        </div>
      </div>
    </div>
    <br /><br /><br />
    <h3 class="titulo">DICTIONARY OF VERBS</h3>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-11">
        <tablaTC
          :cuestionario="tablaUnoPag45"
          class="overflow-auto"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
    </div>
    <br /><br />
    <div class="row">
      <p class="subTitulo marginn-left">
        <i>
          <b>PRACTICE</b>
        </i>
      </p>
    </div>
    <div class="row">
      <p class="parrafoBlack marginn-left text-center">
        <b>Vocabulary:</b>
      </p>
      <br />
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <ul>
        <li
          v-for="item in frasesPag46"
          class="text-left parrafoBlack"
          v-html="item"
        ></li>
      </ul>
    </div>
    <div class="row">
      <p class="parrafoBlack marginn-left text-center">
        <b>Meet – Sell -Throw – Break – Realize</b>
      </p>
      <br />
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <div
          v-for="(item, index) in frases1Pag46"
          :class="'row col-sm-'+item.tamano"
          style="margin-bottom: 0.5em"
        >
          <div v-if="item.name == 'ice'"><inputCE :object="item" /></div>
          <div v-else-if="item.name == 'ic'">
            <inputChecked
              :resuelto="false"
              style="margin-right: 10px; display: inline-flex"
              :esperado="item.lista1"
              :conTexto="true"
              :textoA="item.textoA"
              :textoD="item.textoD"
            />
          </div>
        </div>
      </div>
    </div>

    <div class="row">
      <p class="parrafoBlack marginn-left text-center">
        <b>Say – Think – Buy – Keep – Drink</b>
      </p>
      <br />
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <div
          v-for="(item, index) in frases2Pag46"
          :class="'row col-sm-' + item.tamano"
          style="margin-bottom: 0.5em"
        >
          <div v-if="item.name == 'ice'"><inputCE :object="item" /></div>
          <div v-else-if="item.name == 'ic'">
            <inputChecked
              :resuelto="false"
              style="margin-right: 10px; display: inline-flex"
              :esperado="item.lista1"
              :conTexto="true"
              :textoA="item.textoA"
              :textoD="item.textoD"
            />
          </div>
        </div>
      </div>
    </div>


   
    
  </div>
</template>

<script>
import posiblesRespuestasTabla from "./posiblesRespuestasTabla";
import listaIndex from "./listaIndex";
import inputChecked from "./inputChecked";
import inputCE from "./inputCEnriquecido";
import tablaTC from "./tablaTraduccionCodigos";
import opcionMultiple from "./opcionMultiple"
export default {
  components: {
    listaIndex,
    inputChecked,
    inputCE,
    posiblesRespuestasTabla,
    tablaTC,
    opcionMultiple
  },
  data() {
    return {

       
            respuestasCuestionarioP44: ["B", "A", "A","C","B", "A"],
            cuestionarioP44: [{
                    respuesta: "",
                    pregunta: "1. Where did you buy it?" ,
                      options: [{
                            text: "A. ¿Dónde lo compras?",
                            value: "A",
                            disabled: false,
                        },
                        {
                            text: "B. ¿Dónde lo compraste?",
                            value: "B",
                            disabled: false,
                        },
                         {
                            text: "C. ¿Dónde lo comprarías?",
                            value: "C",
                            disabled: false,
                        },
                      ],
                    
                },
                     
                {
                    respuesta: "",
                    pregunta: "2. What do you teach?",
                    audio: "",
                    options: [{
                            text: "A. ¿Qué enseñas?",
                            value: "A",
                            disabled: false,
                        },
                        {
                            text: "B. ¿Qué enseñaste?",
                            value: "B",
                            disabled: false,
                        },
                         {
                            text: "C. ¿Qué enseñaras?",
                            value: "C",
                            disabled: false,
                        },
                    ],
                },
                {
                    respuesta: "",
                    pregunta: "3. How does she feel?",
                    audio: "",
                    options: [{
                            text: "A. ¿Cómo se siente ella?",
                            value: "A",
                            disabled: false,
                        },
                        {
                            text: "B. ¿Cómo se sintió ella?",
                            value: "B",
                            disabled: false,
                        },
                         {
                            text: "C. ¿Cómo está ella?",
                            value: "C",
                            disabled: false,
                        },
                    ],
                },
                {
                    respuesta: "",
                    pregunta: "4. Why do you love me?",
                    audio: "",
                    options: [{
                            text: "A. ¿Por qué me amabas? ",
                            value: "A",
                            disabled: false,
                        },
                        {
                            text: "B. ¿Qué amas?",
                            value: "B",
                            disabled: false,
                        },
                         {
                            text: "C. ¿Por qué me amas?",
                            value: "C",
                            disabled: false,
                        },
                    ],
                },
                 {
                    respuesta: "",
                    pregunta: "5. When will you come? ",
                    audio: "",
                    options: [{
                            text: "A. ¿Cuándo viniste? ",
                            value: "A",
                            disabled: false,
                        },
                        {
                            text: "B. ¿Cuándo vendrás? ",
                            value: "B",
                            disabled: false,
                        },
                         {
                            text: "C. ¿Cuándo vendrías?",
                            value: "C",
                            disabled: false,
                        },
                    ],
                },
                 {
                    respuesta: "",
                    pregunta: "6. What would we do? ",
                    audio: "",
                    options: [{
                            text: "A. ¿Qué haríamos? ",
                            value: "A",
                            disabled: false,
                        },
                        {
                            text: "B. ¿Qué hicimos? ",
                            value: "B",
                            disabled: false,
                        },
                         {
                            text: "C. ¿Qué haremos?",
                            value: "C",
                            disabled: false,
                        },
                    ],
                },
             
            ],
      
      frases1Pag44: [
        {
          lista1: ["What did you eat"],

          textoA: "YOU/WHAT/DID/EAT? ",
          textoD: "?",

          name: "ic",
          tamano:10
        },
        {
          lista1: ["where would she go"],

          textoA: "GO?/SHE/WHERE/WOULD ",
          textoD: "?",

          name: "ic",
          tamano:10
        },
        {
          lista1: ["How do you feel"],

          textoA: "HOW/DO/FEEL/YOU/? ",

          textoD: "?",
          name: "ic",
          tamano:10
        },
        {
          lista1: ["did"],

          textoA: "1. ¿Cómo te fue? How Go ",
          textoD: "it go?",

          name: "ic",
          tamano:5
        },
        {
          lista1: ["does"],

          textoA: "2. ¿Dónde vive ella? Where  ",

          textoD: "she live?",
          name: "ic",
          tamano:6
        },
        {
          lista1: ["will "],

          textoA: "3. ¿Cuándo me devolverás mi carro? When ",

          textoD: "you bring my car back?",
          name: "ic",
          tamano:8
        },
        {
          lista1: ["do"],

          textoA: "4. ¿Qué quieres de mi? What  ",

          textoD: "you want from me?",
          name: "ic",
          tamano:7
        },
        {
          lista1: ["would"],

          textoA: "5. ¿Qué te gustaría cambiar de tu vida? What ",

          textoD: " you like to change of your life?",
          name: "ic",
          tamano:9
        },
        {
          lista1: [" did"],

          textoA: "6. ¿Cuándo llegaste a Grecia? When ",

          textoD: "you arrive in Greece?",
          name: "ic",
          tamano:8
        },
        {
          lista1: [" will "],

          textoA: "7. ¿A dónde iras de vacaciones en verano? Where ",

          textoD: " you go away to this summer?",
          name: "ic",
          tamano:10
        },
        {
          lista1: [" did"],

          textoA: "8. ¿Cómo lo hiciste? How   ",

          textoD: "you do it?",
          name: "ic",
          tamano:6
        },
        {
          lista1: [" would "],

          textoA:
            "9. ¿Cuánto tiempo te gustaría quedarte con nosotros? How long ",

          textoD: "you like to stay with us?",
          name: "ic",
          tamano:11
        },
        {
          lista1: ["does"],

          textoA: "10. ¿Por qué ella te odia? Why   ",

          textoD: "she hate you?",
          name: "ic",
          tamano:7
        },
        {
          lista1: [" did"],

          textoA: "11. ¿Dónde la conociste? Where ",

          textoD: "you meet her?",
          name: "ic",
          tamano:7
        },
        {
          lista1: [" do"],

          textoA: "12. ¿Qué opinas? What   ",

          textoD: "you think?",
          name: "ic",
          tamano:5
        },
        {
          lista1: ["When"],

          textoA: "13. ¿Cuándo será?  ",

          textoD: " will it be?",
          name: "ic",
          tamano:5
        },
      ],
      tablaUnoPag45: {
        fields: [
          { key: "A", label: "VERB", thClass: "Yellow" },

          { key: "B", label: "PAST AND PARTICIPLE", thClass: " Red" },
          { key: "C", label: "TRANSLATION", thClass: "Blue" },
          {
            key: "complejo2",
            label: "complete with the right form of the verb",
            thClass: " Green",
          },
        ],
        items: [
          {
            A: "THINK",
            B: "Thought-thought",
            C: "Pensar, creer, opinar, considerar ",
            complejo2: {
              lista: ["think"],
              tamano: 20,
              textoA: " I  ",
              textoD: "of you as my friend ",
            },
          },
          {
            A: "BUY   ",
            B: "Bought-bought ",
            C: "  Comprar",
            complejo2: {
              lista: ["bought "],
              tamano: 20,
              textoA: "I have ",
              textoD: " a car recently",
            },
          },
          {
            A: " LET  Permitir  ",
            B: "Let-let ",
            C: " dejar",
            complejo2: {
              lista: [" let"],
              tamano: 20,
              textoA: "She didn´t   ",
              textoD: "me go ",
            },
          },
          {
            A: "DENY  ",
            B: " Regular",
            C: " Negar, rechazar, desmentir",
            complejo2: {
              lista: ["denied "],
              tamano: 22,
              textoA: "He ",
              textoD: "damaging the car ",
            },
          },
          {
            A: " BREATHE  ",
            B: " Regular",
            C: "Respirar ",
            complejo2: {
              lista: ["breathe "],
              tamano: 20,
              textoA: "I can´t ",
              textoD: " deeply ",
            },
          },
          {
            A: " DREAM ",
            B: " Dreamt-dreamt ",
            C: "Soñar ",
            complejo2: {
              lista: ["dream "],
              tamano: 21,
              textoA: "What did you  ",
              textoD: "  about?",
            },
          },
          {
            A: "AVOID ",
            B: " Regular",
            C: "Evitar, evadir ",
            complejo2: {
              lista: [" avoid"],
              tamano: 23,
              textoA: " I ",
              textoD: "eating fast food at night ",
            },
          },
          {
            A: " REALIZE  ",
            B: " Regular",
            C: " Darse cuenta, realizar",
            complejo2: {
              lista: [" realize"],
              tamano: 20,
              textoA: " How did you",
              textoD: " ?",
            },
          },
          {
            A: " SELL  ",
            B: "Sold-sold ",
            C: "Vender ",
            complejo2: {
              lista: [" sold"],
              tamano: 22,
              textoA: "I haven´t ",
              textoD: "my car yet ",
            },
          },
          {
            A: "HELP ",
            B: "Regular ",
            C: "  Ayudar-socorrer",
            complejo2: {
              lista: ["help "],
              tamano: 23,
              textoA: "I am sorry, I can’t  ",
              textoD: "  you now ",
            },
          },
          {
            A: "KNOW ",
            B: "Knew-known ",
            C: "Saber-conocer ",
            complejo2: {
              lista: ["know "],
              tamano: 26,
              textoA: "She doesn’t ",
              textoD: "anything about me ",
            },
          },
          {
            A: " MEET ",
            B: "Met-met ",
            C: " Encontrarse con, conocer, presentar",
            complejo2: {
              lista: ["met "],
              tamano: 26,
              textoA: "I  ",
              textoD: "a nice girl a couple days ago ",
            },
          },
          {
            A: " ACHIEVE  ",
            B: " Regular",
            C: "Lograr, obtener, conseguir ",
            complejo2: {
              lista: [" achieved"],
              tamano: 22,
              textoA: " I",
              textoD: "a pay rise last year ",
            },
          },
          {
            A: "SAY  ",
            B: "Said-said ",
            C: " Decir",
            complejo2: {
              lista: ["said "],
              tamano: 20,
              textoA: "I haven´t ",
              textoD: "anything ",
            },
          },
          {
            A: "KEEP ",
            B: " Kept-kept",
            C: " Guardar, conservar, mantener, continuar, cumplir",
            complejo2: {
              lista: ["kept  "],
              tamano: 18,
              textoA: " I always",
              textoD: "  my word",
            },
          },
          {
            A: " TRY ",
            B: " Regular",
            C: "Intentar, probar, hacer el esfuerzo ",
            complejo2: {
              lista: [" tried"],
              tamano: 26,
              textoA: " She",
              textoD: "to fix the car this morning ",
            },
          },
          {
            A: "WANT  ",
            B: " Regular",
            C: "Querer, desear ",
            complejo2: {
              lista: ["wanted "],
              tamano: 22,
              textoA: "She ",
              textoD: "to be an actress ",
            },
          },
          {
            A: " NEED  ",
            B: "Regular ",
            C: " Necesitar",
            complejo2: {
              lista: ["needed "],
              tamano: 18,
              textoA: " I",
              textoD: "it yesterday ",
            },
          },
          {
            A: "DRINK",
            B: "Drank-drunk  ",
            C: "  Beber-tomar",
            complejo2: {
              lista: [" drunk"],
              tamano: 23,
              textoA: "I had never",
              textoD: "vodka before  ",
            },
          },
          {
            A: "MISS ",
            B: " Regular",
            C: "Perder, extrañar, fallar ",
            complejo2: {
              lista: [" miss"],
              tamano: 23,
              textoA: " I",
              textoD: " you every night and day",
            },
          },
          {
            A: "COME  ",
            B: "Came-come ",
            C: "Venir ",
            complejo2: {
              lista: [" come"],
              tamano: 22,
              textoA: " I have",
              textoD: "  to say good bye ",
            },
          },
          {
            A: " GRAB ",
            B: " Regular",
            C: " Agarrar, coger",
            complejo2: {
              lista: [" grab"],
              tamano: 22,
              textoA: "Could you ",
              textoD: "this for me? ",
            },
          },
        ],
      },
      frasesPag46: [
        "Bill: cuentas / Along: a lo largo de / Slowly: despacio / Back-left: la izquierda de atrás / Get married: casarse /",
        "Look at: observar / Over there: allá / Outside: afuera <br><br><br>",
        "Usa uno de estos verbos para completar la oración y asegúrate que este ",
      ],

      frases1Pag46: [
        {
          lista1: ["realize"],

          textoA: "1. How did you  ",
          textoD: "that I was under this mask?",

          name: "ic",
          tamano:6
        },
        {
          lista1: ["sell"],

          textoA:
            "2. The financial crisis is affecting our standard of life so I´ll have to  ",
          textoD: "my car to pay bills",

          name: "ic",
          tamano:9
        },
        {
          lista1: ["threw"],
          lista2: ["to"],
          tamano:11,
          textoA:
            "3. I was driving my car along the street very slowly when a boy   ",
          textoD2: "broke my back-left window.",
          textoD: "a rock at me and",
          name: "ice",
        },
        {
          lista1: ["met"],

          textoA: "4. It has been 5 years now since we ",
          textoD: ".– Happy anniversary.",
          tamano:7,
          name: "ice",
        },
      ],
      frasesPag46: [
        "Bill: cuentas / Along: a lo largo de / Slowly: despacio / Back-left: la izquierda de atrás / Get married: casarse /",
        "Look at: observar / Over there: allá / Outside: afuera <br><br><br>",
        "Usa uno de estos verbos para completar la oración y asegúrate que este ",
      ],

      frases2Pag46: [
        {
          lista1: ["kept"],

          textoA:
            "1. I worked for about 16 hours in a row to finish my project and the next day I ",
          textoD: "on working for another 2 hours. ",
          tamano:11,
          name: "ic",
        },
        {
          lista1: ["buy"],

          textoA:
            "2. Look at that nice blue car over there! It is for sale. Let´s go and ask for the price and if it is not expensive I will",
          textoD: "it.",
          tamano:11,
          name: "ic",
        },
        {
          lista1: ["say"],

          textoA: "3. I am so sorry! I wasn’t listening. What did you ?",
          tamano:6,
          textoD: "",
          name: "ice",
        },
        {
          lista1: ["thought"],

          textoA:
            "4. Where are you Matt? – I am outside of your house! – oh no! I ",
          textoD: " you were home. I am outside of your house too. ",
          tamano:11,
          name: "ice",
        },
        {
          lista1: ["drunk"],

          textoA: "5. Have you ever  ",
          textoD: " whisky? – no, I have never tried it and I don’t want to  ",
          tamano:8,
          name: "ice",
        },
      ],
     
    };
  },
};
</script>
<style scoped>
.show-grid {
  border: 1px solid;
  color: black;
}

#text,
#inputText {
  text-align: left;
}

/deep/ .Blue {
  background-color: cornflowerblue;
}
/deep/ .Red {
  background-color: crimson;
}
/deep/ .Yellow {
  background-color: yellow;
}
/deep/ .Green {
  background-color: chartreuse;
}

/deep/ .noHead {
  border-width: 0;
  font-size: 0;
}
/deep/ .Subrayado {
  text-decoration-line: underline;
}

inputChecked {
  display: inline-flex;
}
</style>