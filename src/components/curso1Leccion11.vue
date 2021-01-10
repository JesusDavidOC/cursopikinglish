<template>
  <div>
    <br><br>
      <div class="row">
        <div class="col-sm-1"></div>
      <i class="fa fa-diamond marginn-left" style="font-size: 1.5em"></i>

      <p class="fuenteDiamond marginn-left">
        Ubica el modificador DO-DOES-DID-WILL O WOULD más el verbo en
          presente.
      </p>
      <br />
    </div>
     <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-11">
        <tablaTC
          class=" botTabla"
          :cuestionario="tablaPag47"
          
        />
      </div>
      
    </div>


       <div class="row">
         <div class="col-sm-1"></div>
      <i class="fa fa-diamond marginn-left" style="font-size: 1.5em"></i>

      <p class="fuenteDiamond marginn-left">
        
        EJERCICIOS LÓGICOS PARA PRACTICAR MODIFICADORES
      </p>
      <br />
    </div>
      <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-11 row">
        <div class="col-sm-1 " id="tabla">
          <listaIndex :tabla="$data.tablaAPag48" />
        </div>
        <div class="col-sm-2 " id="tabla">
          <listaIndex :tabla="$data.tablaBPag48" />
        </div>

        <div class="col-sm-2 " id="tabla">
          <listaIndex :tabla="$data.tablaCPag48" />
        </div>

        <div class="col-sm-2 " id="tabla">
          <listaIndex :tabla="$data.tablaDPag48" />
        </div>
        
        <div class="col-sm-2 " id="tabla">
          <listaIndex :tabla="$data.tablaEPag48" />
        </div>

      
      </div>
    </div>
   
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-8">
        <tablaTC
          :cuestionario="$data.cuestionario1Pag48"
          :inglesR="false"
          :espanolR="true"
         
        />
      </div>
    </div>
    <br />
    <br />
    <br />
    <div class="row container">
      <div class="col-md-1"></div>
      <b-col md="10" class="titulo">
        <h3>IRREGULAR VERBS IN PAST</h3>
      </b-col>
    </div>
    
    <img src="/cursos/curso1/leccion11/imagenes/tablaPag49.png" />

    <div class="row">
      <p class="subTitulo marginn-left">
        
          UN VERBO SE USA EN SU FORMA PASADA SOLO EN AFIRMACIÓN.
        
      </p>
    </div>
    <br />
    <br />
    <br />
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <tablaTC
          class="overflow-auto parrafoBlack"
          :cuestionario="tabla1P49"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
    </div>
    <br /><br /><br />
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 ">
        <div
          v-for="(item, index) in frases1Pag49"
          
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
              :tamano="item.tamano"
            />
          </div>
        </div>
      </div>
    </div>
    <br /><br /><br />





  </div>
</template>

<script>
import posiblesRespuestasTabla from "./posiblesRespuestasTabla";
import listaIndex from "./listaIndex";
import inputChecked from "./inputChecked";
import inputCE from "./inputCEnriquecido";
import tablaTC from "./tablaTraduccionCodigos";
export default {
  components: {
    listaIndex,
    inputChecked,
    inputCE,
    posiblesRespuestasTabla,
    tablaTC,
  },
  data() {
    return {
        tablaPag47: {
        fields: [
          { key: "A", label: "A", thClass: "noHead" },
          { key: "complejo21", label: "A", thClass: "noHead" },
        ],
        items: [
         
        {
          A: "1. ¿Dónde pagas los servicios? ",
          complejo21: {
          lista1: ["do"],
          lista2: ["pay"],
          textoA: "Where  ",
          textoD: "you ",
          textoD2: "utilities?",
          name: "ice",
          tamano1:15,
          tamano2:15,
          }
        },
        {
          A: "2. ¿Qué lograste?",
          complejo21: {
          lista1: ["did"],
          lista2: ["achieve"],
          textoA: " What   ",
          textoD: "you ",
          textoD2: "?",
          name: "ice",
          tamano1:15,
          tamano2:13,
          }
        },
        {
          A: "3. ¿Entendiste lo que ella dijo?",
          complejo21: {
          lista1: ["Did"],
          lista2: ["understand"],
          textoA: "    ",
          textoD: "you ",
          textoD2: "what she said?",
          name: "ice",
          tamano1:13,
          tamano2:23,
          }
        },
        {
          A: "4. ¿Qué pensaste sobre lo que te dije?",
          complejo21: {
          lista1: ["did"],
          lista2: ["think"],
          textoA: " What ",
          textoD: "you ",
          textoD2: "about what I told you?",
          name: "ice",
          tamano1:15,
          tamano2:23,
          }
        },
        {
          A: "5. ¿Por qué robaste ese carro?",
          complejo21: {
          lista1: ["did"],
          lista2: ["steal"],
          textoA: "Why    ",
          textoD: "you ",
          textoD2: " that car? ",
          name: "ice",
          tamano1:14,
          tamano2:16,
          }
        },
        {
          A: "6. ¿Ella Te Negó?",
          complejo21: {
          lista1: ["Did"],
          lista2: ["deny"],
          textoA: "  ",
          textoD: "she ",
          textoD2: "you?",
          name: "ice",
          tamano1:12,
          tamano2:14,
          }
        },
        {
          A: "7. ¿Marcos Respira Bien?",
          complejo21: {
          lista1: ["Does"],
          lista2: ["breathe"],
          textoA: "     ",
          textoD: "Marcos ",
          textoD2: "Well?",
          name: "ice",
          tamano1:15,
          tamano2:15,
          }
        },
        {
          A: "8. ¿Tú Juras Por Dios?",
          complejo21: {
          lista1: ["Do"],
          lista2: ["swear"],
          textoA: "  ",
          textoD: "you ",
          textoD2: "to God?",
          name: "ice",
          tamano1:11,
          tamano2:16,
          }
        },
        {
          A: "9. ¿Por qué no lo evitaste?",
          complejo21: {
          lista1: ["did"],
          lista2: ["avoid"],
          textoA: " Why  ",
          textoD: "you not ",
          textoD2: "it?",
          name: "ice",
          tamano1:17,
          tamano2:12,
          }
        },
        {
          A: "10. ¿Qué te robaste?",
          complejo21: {
          lista1: ["did"],
          lista2: ["steal"],
          textoA: " What",
          textoD: "you ",
          textoD2: "?",
          name: "ice",
          tamano1:15,
          tamano2:12,
          }
        },
        {
          A: "11.¿Cuándo vendiste tu carro?",
          complejo21: {
          lista1: ["did "],
          lista2: ["sell"],
          textoA: " When ",
          textoD: "you ",
          textoD2: "your car?",
          name: "ice",
          tamano1:15,
          tamano2:15,
          }
        },
        {
          A: "12.¿Que necesitas?",
          complejo21: {
          lista1: ["do"],
          lista2: ["need"],
          textoA: "What ",
          textoD: "you ",
          textoD2: "?",
          name: "ice",
          tamano1:14,
          tamano2:11,
          }
        },
        {
          A: "13.¿Cuándo la conociste?",
            complejo21: {
          lista1: [" did "],
          lista2: ["meet"],
          textoA: "When  ",
          textoD: "you ",
          textoD2: "",
          name: "ice",
          tamano1:15,
          tamano2:11,
            }
        },
        {
          A: "14.¿Dónde lo intentarías?",
          complejo21: {
          lista1: ["would"],
          lista2: [" try"],
          textoA: "Where   ",
          textoD: "you ",
          textoD2: "it?",
          name: "ice",
          tamano1:17,
          tamano2:11,
          }
        },
        {
          A: "15.¿Me extrañas?",
          complejo21: {
          lista1: ["Do"],
          lista2: [" miss"],
          textoA: "  ",
          textoD: "you ",
          textoD2: "me?",
          name: "ice",
          tamano1:12,
          tamano2:13,
          }
        },
        {
          A: "16.¿Porque me culpaste?",
          complejo21: {
          lista1: ["did"],
          lista2: [" blame"],
          textoA: "Why  ",
          textoD: "you ",
          textoD2: " me?",
          name: "ice",
          tamano1:14,
          tamano2:14,
          }
        },
        {
          A: "17.¿Cuándo vendrás?",
          complejo21: {
          lista1: ["will"],
          lista2: ["come"],
          textoA: "When   ",
          textoD: "you ",
          textoD2: "?",
          name: "ice",
         tamano1:15,
          tamano2:12,
          }
        },
        {
          A: "18.¿Te negarías a hablar con él?",
          complejo21: {
          lista1: ["Would "],
          lista2: ["deny "],
          textoA: " ",
          textoD: "you ",
          textoD2: "speaking to him?",
          name: "ice",
          tamano1:14,
          tamano2:20,
          }
        },
        {
          A: "19.¿Cómo te diste cuenta?",
          complejo21: {
          lista1: ["How"],
          lista2: ["realize"],
          textoA: "  ",
          textoD: "did you",
          textoD2: "?",
          name: "ice",
         tamano1:15,
          tamano2:12,
          }
        },
        {
          A: "20.¿Dónde lo tiraste?",
          complejo21: {
          lista1: ["Where"],
          lista2: ["throw "],
          textoA: " did ",
          textoD: "you ",
          textoD2: "it?",
          name: "ice",
          tamano1:15,
          tamano2:13,
          }
        },
        {
          A: "21. ¿Con quién vives?",
          complejo21: {
          lista1: ["do"],
          lista2: ["live "],
          textoA: "Who   ",
          textoD: "you ",
          textoD2: "with?",
          name: "ice",
          tamano1:14,
          tamano2:13,
          }
        },
        {
          A: "22. ¿Qué opinas?",
          complejo21: {
          lista1: ["do"],
          lista2: ["think"],
          textoA: "What   ",
          textoD: "you ",
          textoD2: "?",
          name: "ice",
          tamano1:14,
          tamano2:11,
          }
        },
      ]
    },

           
            tablaAPag48: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "A", thClass: "Yellow noHead " },
        ],

        items: [
          { A: " WHAT" },
          { A: " WHERE " },
          { A: " WHY" },
          { A: " WHEN" },
          { A: " HOW" },
          { A: " WHO" },
          { A: "WHAT TIME " },
          
        ],
      },

      tablaBPag48: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "B", thClass: "Red noHead" },
        ],
        items: [
          { B: " DO" },
          { B: " DOES" },
          { B: " DID" },
          { B: "  WILL" },
          { B: " WOULD" },
        
        ],
      },
      tablaCPag48: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "C", thClass: "Blue noHead" },
        ],

        items: [
          { C: " I" },
          { C: " YOU" },
          { C: "SHE" },
          { C: "HE" },
          { C: "IT" },
          { C: " WE" },
          { C: "THEY" },
         
        ],
      },
        tablaDPag48: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "A", thClass: "Green noHead " },
        ],

        items: [
          { A: " EAT" },
          { A: " FEEL " },
          { A: "   LOVE" },
          { A: "COME" },
          { A: " STUDY" },
          { A: "LIVE" },
          { A: " GO" },
          {A:"SAY"},
          {A:"STEAL"},
          {A:"SEE"},
          {A:"WANT"}
        ],
      },

      tablaEPag48: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items
          
          // A column that needs custom formatting
          { key: "B", thClass: "Blue  " },
        ],
        items: [
          { B: "12.NEED" },
          { B: "13. CALL ME" },
          { B: "14. GROW UP" },
          { B: "15. DO" },
          { B: "16. SLEEP" },
          { B: "17. BUY" },
          { B: "18. WAKE UP" },
          { B: "19. WRITE " },
          { B: "20. HEAR " },
          { B: " 21. ARRIVE" },
          { B: "22. WORK " },
        
          
        ],
      },
        

      cuestionario1Pag48: {
        fields: [
          { key: "A", thClass: "Blue parrafoBlack" },
          { key: "B", thClass: "Red parrafoBlack" },
          { key: "C", thClass: "Yellow parrafoBlack" },
          { key: "D", thClass: "Green parrafoBlack" },
          { key: "complejo1", label: "ENGLISH" },
          { key: "E", label: "SPANISH" },
        ],
        items: [
          {
            A: 3,
            B: 3,
            C: 2,
            D: 4,
            complejo1: { lista: ["Why did you come?"], tamano: 25 },
            E: "¿Por qué viniste? ",
          },
          {
            A: 2,
            B: 2,
            C: 3,
            D: 6,
            complejo1: { lista: ["Where does she live?"], tamano: 25 },
            E: "¿Dónde vive ella?",
          },
          {
            A: 2,
            B: 3,
            C: 2,
            D: 14,
            complejo1: { lista: ["Where did you grow up"], tamano: 25 },
            E: "¿Dónde creciste?",
          },
          {
            A: 5,
            B: 1,
            C: 2,
            D: 2,
            complejo1: { lista: ["How do you feel?"], tamano: 25 },
            E: "¿Comó te sientes?",
          },
          {
            A: 4,
            B: 4,
            C: 2,
            D: 4,
            complejo1: { lista: ["When will you come?"], tamano: 25 },
            E: "¿Cuándo vendrás?",
          },
          {
            A: 7,
            B: 4,
            C: 6,
            D: 21,
            complejo1: { lista: ["What time will we arrive?"], tamano: 25 },
            E: "¿A qué horas llegaremos?",
          },
          {
            A: 5,
            B: 3,
            C: 2,
            D: 16,
            complejo1: { lista: ["How did you sleep?"], tamano: 25 },
            E: "¿Cómo dormiste?",
          },
          {
            A: 1,
            B: 1,
            C: 2,
            D: 11,
            complejo1: { lista: ["What do you want?"], tamano: 25 },
            E: "¿Qué quieres?",
          },
          {
            A: 1,
            B: 5,
            C: 2,
            D: 19,
            complejo1: { lista: ["What would you write?"], tamano: 25 },
            E: "¿Qué escribirías?",
          },
          {
            A: 1,
            B: 3,
            C: 2,
            D: 10,
            complejo1: { lista: ["What did you see?"], tamano: 25 },
            E: "¿Qué viste?",
          },
          {
            A: 2,
            B: 1,
            C: 2,
            D: 22,
            complejo1: { lista: ["Where do you work?"], tamano: 25 },
            E: "¿Dónde trabajas?",
          },
          {
            A: 7,
            B: 2,
            C: 4,
            D: 18,
            complejo1: { lista: ["What time does he wake up?"], tamano: 25 },
            E: "¿A qué horas él se despierta?",
          },
          {
            A: 4,
            B: 4,
            C: 2,
            D: 13,
            complejo1: { lista: ["When will they call me?"], tamano: 25 },
            E: "¿Cuándo ellos me llamarán?",
          },
          {
            A: 2,
            B: 3,
            C: 2,
            D: 5,
            complejo1: { lista: ["Where did you study?"], tamano: 25 },
            E: "¿Dónde estudiaste?",
          },
          {
            A: 1,
            B: 2,
            C: 3,
            D: 15,
            complejo1: { lista: ["What does she do?"], tamano: 25 },
            E: "¿Qué hace ella?",
          },
          {
            A: 6,
            B: 3,
            C: 2,
            D: 3,
            complejo1: { lista: ["Who do you Love?"], tamano: 25 },
            E: "¿A quién amas?",
          },
          {
            A: 2,
            B: 3,
            C: 3,
            D: 14,
            complejo1: { lista: ["Where did she grow up"], tamano: 25 },
            E: "¿Dónde creció ella?",
          },
          {
            A: 4,
            B: 4,
            C: 2,
            D: 7,
            complejo1: { lista: ["When will you go?"], tamano: 25 },
            E: "¿Cuándo iras?",
          },
        ],
      },
      tabla1P49: {
        fields: [
          {
            key: "A",
            label: "Irregular verbs",
            thClass: "Red Subrayado parrafoWhite",
          },
          { key: "B", label: "", thClass: "" },
          {
            key: "C",
            label: "Regular verbs",
            thClass: "Red Subrayado parrafoWhite",
          },
          { key: "D", label: "", thClass: "" },
        ],
        items: [
          {
            A: "I went to Cali   ",
            B: "Yo fui a Cali",
            C: " I played well",
            D: "Yo jugué bien",
          },
          {
            A: "I ate an apple    ",
            B: "Yo me comí una manzana",
            C: "I worked hard",
            D: "Yo trabajé duro",
          },
          {
            A: "I took a taxi  ",
            B: "Yo tomé un taxi",
            C: "I studied english",
            D: " Yo estudié inglés ",
          },
          {
            A: "I bought a ticket  ",
            B: "Compré un boleto",
            C: " I cleaned the house",
            D: "Yo limpié la casa ",
          },
          {
            A: "I did exercise  ",
            B: "Yo hice ejercicio",
            C: "I smiled very much",
            D: " Yo sonreí mucho ",
          },
          {
            A: " I saw a movie  ",
            B: "Yo vi una película",
            C: "I fried an egg",
            D: " Yo frité un huevo",
          },
        ],
      },
      frases1Pag49: [
        {
          lista1: ["saw"],

          textoA: "1.<strong>  Ella vio a su madre:</strong>  She ",
          textoD: "her mother (see/saw)",
          tamano:39,
          name: "ic",
        },
        {
          lista1: ["ate"],

          textoA: "2. <strong> Yo comí mucho:</strong> I  ",
          textoD: "very much (eat/ate)",

          name: "ic",
          tamano:33
        },
        {
          lista1: ["fell"],

          textoA: "3.<strong>  El niño se cayó de la cama: </strong>The boy",

          textoD: "off the bed (fall/fell)",
          name: "ic",
          tamano:44
        },
        {
          lista1: ["did"],

          textoA: "4.<strong>  Natalie hizo deporte ayer: </strong>Natalie",
          textoD: "sport yesterday (do/did) (UK)",

          name: "ic",
          tamano:48
        },
        {
          lista1: ["went"],

          textoA: "5.<strong>  Yo fui a trabajar esta mañana:</strong> I",

          textoD: "to work this morning (go/ went)",
          name: "ic",
          tamano:49
        },
        {
          lista1: ["bought "],

          textoA: "6. <strong> Ella compró un carro:</strong> She  ",

          textoD: "a car (buy/bought)",
          name: "ic",
          tamano:40
        },
        {
          lista1: ["thought"],

          textoA: "7. <strong> Yo pensé en mi madre:</strong> I  ",

          textoD: "of my mother (think/ thought)",
          name: "ic",
          tamano:45
        },
        {
          lista1: ["had"],

          textoA: "8.<strong>  Tuvimos un buen día:</strong> we",

          textoD: "a good day (have/ had)",
          name: "ic",
          tamano:40
        },
        {
          lista1: ["gave"],

          textoA: "9.<strong>  Mi mamá me dio esto: </strong>my mother ",

          textoD: "me this (give/gave)",
          name: "ic",
          tamano:43
        },
        {
          lista1: [" taught "],

          textoA: "10.<strong> El profesor nos enseñó muy bien:</strong> the teacher ",

          textoD: " us very well (teach/taught)",
          name: "ic",
          tamano:57
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
/deep/ .Subrayado {
  text-decoration-line: underline;
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

inputChecked {
  display: inline-flex;
}
/deep/ .row{
  margin-left: 0%;
  margin-right: 0%;
}
</style>