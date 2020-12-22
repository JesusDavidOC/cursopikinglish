<template>
  <div>
   
     <div class="row">
       <div class="col-sm-1"></div>
      <i class="fa fa-diamond marginn-left" style="font-size: 1.5em"></i>

      <p class="fuenteDiamond marginn-left">
        &nbsp;
        Ejercicios lógicos con auxiliares negativos.
      </p>
      <br />
    </div>
        <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-11 row">
        <div class="col-sm-1 " id="tabla">
          <listaIndex :tabla="$data.tablaAPag41" />
        </div>
        <div class="col-sm-2 " id="tabla">
          <listaIndex :tabla="$data.tablaBPag41" />
        </div>

        <div class="col-sm-2 " id="tabla">
          <listaIndex :tabla="$data.tablaCPag41" />
        </div>

        <div class="col-sm-2 " id="tabla">
          <listaIndex :tabla="$data.tablaDPag41" />
        </div>
        <div class="col-sm-1"></div>
        <div class="col-sm-2 " id="tabla">
          <listaIndex :tabla="$data.tablaEPag41" />
        </div>

        <div class="col-sm-2 " id="tabla">
          <listaIndex :tabla="$data.tablaFPag41" />
        </div>
      </div>
    </div>
    <br><br>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-7">
        <tablaTC
          :cuestionario="$data.cuestionario1Pag41"
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
        <h3>EL USO DE LA PALABRA “TO”</h3>
      </b-col>
    </div>
     <br>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-11 row">
        <div class="col-sm-10 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaAPag42" />
        </div>
        
      </div>
    </div>
      <b-row>
   
      <b-col md="10" >
        <p class="subTitulo marginn-left">
          PRACTICE
        </p>
         
        </b-col>
</b-row>
    
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-11 ">
        <div
          v-for="(item, index) in frases1Pag42"
          
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
    <img src="/cursos/curso1/leccion9/imagenes/tablaPag43.png" />
    <br><br>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-7">
        <tablaTC
          :cuestionario="$data.cuestionario1Pag43"
          :inglesR="false"
          :espanolR="true"
        />
      </div>
    </div>
    <br />
    <br />
    <br />
    
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
        tablaAPag41: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "A", thClass: "Yellow noHead " },
        ],

        items: [
          { A: " I" },
          { A: " You " },
          { A: " She" },
          { A: " He" },
          { A: " It" },
          { A: " They" },
          { A: "We " },
          { A: " Sam" },
        ],
      },

      tablaBPag41: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "B", thClass: "Red noHead" },
        ],
        items: [
          { B: " Don't" },
          { B: " Doesn't" },
          { B: " Didn't" },
          { B: "  Won't" },
          { B: " Wouldn´t" },
        
        ],
      },
      tablaCPag41: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "C", thClass: "Blue noHead" },
        ],

        items: [
          { C: " Do" },
          { C: " Have" },
          { C: " Say" },
          { C: " Live" },
          { C: " Feel" },
          { C: " Work" },
          { C: " Go" },
          { C: " Hate" },
        ],
      },
        tablaDPag41: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "A", thClass: "Green noHead " },
        ],

        items: [
          { A: " Anything" },
          { A: " Anywhere " },
          { A: "  Here" },
          { A: " There" },
          { A: "That" },
          { A: "Good" },
          { A: " Yesterday" },
          {A:"Anyone"}
        ],
      },

      tablaEPag41: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "B", thClass: "Blue noHead " },
        ],
        items: [
          { B: " Hacer" },
          { B: " Tener" },
          { B: " Decir" },
          { B: " Vivir" },
          { B: " Sentir" },
          { B: " Trabajar" },
          { B: " Ir" },
          { B: " Odiar" },
          
        ],
      },
      tablaFPag41: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items
          "#",
          // A column that needs custom formatting
          { key: "C", thClass: "Green noHead " },
        ],

        items: [
          { C: " Nada" },
          { C: " Ninguna parte" },
          { C: " Aqui" },
          { C: " Allá" },
          { C: " Eso" },
          { C: " Bien" },
          { C: " Ayer" },
          { C: "Nadie" },
        ],
      },
        
      cuestionario1Pag41: {
        fields: [
          { key: "A", thClass: "Blue parrafoBlack" },
          { key: "B", thClass: "Red parrafoBlack" },
          { key: "C", thClass: "Yellow parrafoBlack" },
          { key: "D", thClass: "Green parrafoBlack" },
          { key: "complejo1", label: "ENGLISH" },
          { key: "E", label: "SPANISH", thClass: "text-left"},
        ],
        items: [
          {
            A: 1,
            B: 1,
            C: 1,
            D: 1,
            complejo1: { lista: ["I do not do anything"], tamano: 25 },
            E: "Yo no hago nada",
          },
          {
            A: 2,
            B: 3,
            C: 7,
            D: 2,
            complejo1: { lista: ["You didn't go anywhere"], tamano: 25 },
            E: "Tú no fuiste a ningún lado",
          },
          {
            A: 3,
            B: 2,
            C: 2,
            D: 5,
            complejo1: { lista: ["She doesn't have that"], tamano: 25 },
            E: "Ella no tiene eso",
          },
          {
            A: 6,
            B: 5,
            C: 1,
            D: 1,
            complejo1: { lista: ["They wouldn't do that"], tamano: 25 },
            E: "Ellos no harían nada",
          },
          {
            A: 1,
            B: 4,
            C: 6,
            D: "",
            complejo1: { lista: ["I won't work"], tamano: 25 },
            E: "Yo no trabajaré",
          },
          {
            A: 1,
            B: 5,
            C: 4,
            D: 3,
            complejo1: { lista: ["I wouldn't live here"], tamano: 25 },
            E: "Yo no viviría aquí",
          },
          {
            A: 1,
            B: 1,
            C: 5,
            D: 6,
            complejo1: { lista: ["I don't feel good"], tamano: 25 },
            E: "Yo no me siento bien",
          },
          {
            A: 2,
            B: 3,
            C: 3,
            D: 1,
            complejo1: { lista: ["You didn't say anything"], tamano: 25 },
            E: "Tú no dijiste nada",
          },
          {
            A: 3,
            B: 2,
            C: 4,
            D: 4,
            complejo1: { lista: ["She doesn't live there"], tamano: 25 },
            E: "Ella no vive allá",
          },
          {
            A: 7,
            B: 4,
            C: 7,
            D: 2,
            complejo1: { lista: ["We won't go anywhere"], tamano: 25 },
            E: "Nosotros no iremos a ningún lado",
          },
          {
            A: 1,
            B: 1,
            C: 6,
            D: 3,
            complejo1: { lista: ["You don't work here"], tamano: 25 },
            E: "Tú no trabajas aquí",
          },
          {
            A: 1,
            B: 3,
            C: 1,
            D: 5,
            complejo1: { lista: ["I didn't do that"], tamano: 25 },
            E: "Yo no hice eso",
          },
          {
            A: 1,
            B: 3,
            C: 2,
            D: 1,
            complejo1: { lista: ["I didn't have that"], tamano: 25 },
            E: "Yo no tenía nada",
          },
          {
            A: 3,
            B: 2,
            C: 2,
            D: 1,
            complejo1: { lista: ["She doesn't have anything"], tamano: 25 },
            E: "Ella no tiene nada",
          },
          {
            A: 3,
            B: 5,
            C: 6,
            D: 2,
            complejo1: { lista: ["She wouldn't work anywhere"], tamano: 25 },
            E: "Ella no trabajaría en ningún lado",
          },
          {
            A: 1,
            B: 1,
            C: 7,
            D: 2,
            complejo1: { lista: ["I don't go anywhere"], tamano: 25 },
            E: "Yo no voy a ningún lado",
          },
          {
            A: 2,
            B: 3,
            C: 3,
            D: 1,
            complejo1: { lista: ["You didn't say anything"], tamano: 25 },
            E: "Tú no dijiste nada",
          },
          {
            A: 3,
            B: 2,
            C: 4,
            D: 4,
            complejo1: { lista: ["She doesn't live there"], tamano: 25 },
            E: "Ella no vive allá",
          },
          {
            A: 1,
            B: 4,
            C: 7,
            D: 2,
            complejo1: { lista: ["I won't go anywhere"], tamano: 25 },
            E: "Yo no iré a ningún lado",
          },
          {
            A: 6,
            B: 5,
            C: 1,
            D: 1,
            complejo1: { lista: ["They don't do anything"], tamano: 25 },
            E: "Ellos no hacen nada",
          },
          {
            A: 1,
            B: 4,
            C: 6,
            D: 3,
            complejo1: { lista: ["I won't work here"], tamano: 25 },
            E: "Yo no trabajaré aquí",
          },
          {
            A: 8,
            B: 2,
            C: 8,
            D: 8,
            complejo1: { lista: ["Sam doesn't hate anyone"], tamano: 25 },
            E: "Sam no odia a nadie",
          },
          {
            A: 3,
            B: 2,
            C: 5,
            D: 6,
            complejo1: { lista: ["They don't feel good"], tamano: 25 },
            E: "Ellas no se sienten bien",
          },
          {
            A: 1,
            B: 4,
            C: 6,
            D: 2,
            complejo1: { lista: ["I don't go anywhere"], tamano: 25 },
            E: "Yo no voy a ningún lado",
          },
        ],
      },
      tablaAPag42: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "A", thClass: "", label: "Para separar dos verbos" },
           { key: "B", thClass: "", label: "Want/ go" },
           { key: "C", thClass: "", label: "I want to go" },
        ],

        items: [
          { A: "Significa “a”",
             B: "Hacia un lugar, desde un punto a otro.",
             C:"I will go to Spain I work from Monday to Friday"
           },
          { A: "Significa “para”",
           B: "para qué algo sirve",
            C: "The money is to buy a house." },
          { A: "Significa “que”",
          B: "Únicamente con el verbo “HAVE”",
          C: "I have to eat more fruits"
          },
          { A: "Hacen parte de algunos verbos simplemente.", B: "Listen to, talk to, lie to, belong to Say to, look forward to. Etc",
          C: "I like to listen to music." },
          { A: "Significa “hasta”",
           B: "Con verbos de movimientos Walk, go, run, drive, swim, fly. Etc",
           C: "I walk to school every day" 
           },
        
          { A: "Significa “por”" ,
          B: "Cuando hay un deseo o un brindis",
          C:
              "I make this toast to Simon who has inspired us to be better human beings.",},
          { A: "Significa “para las" ,
          B: "Si se trata de la hora",
          C: "It is twenty to five"
          },
          { A: "Después de palabras de información",
           B: "What to, where to, how to",
           C: "I don’t know what to do"  },
        ],
      },

      
      frases1Pag42: [
        {
          lista1: ["to"],
          lista2: ["to"],
          textoA: "1. I don’t want",
          textoD: "talk",
          textoD2: "you. <strong>(No quiero hablar contigo)</strong>",
          name: "ice",
          tamano1:19,
          tamano2:27
        },
        {
          lista1: ["to"],

          textoA: "2. It is a quarter",
          textoD: "one. <strong>(Falta un cuarto para la una)</strong>",

          name: "ic",
           tamano:37
        },
        {
          lista1: ["to"],

          textoA: "3. What are you going",

          textoD: "do? <strong>(Qué vas a hacer?)</strong>",
          name: "ic",
           tamano:35
        },
        {
          lista1: ["to"],
          lista2: ["to"],
          textoA: "4. Go ",
          textoD: "the traffic light and give this",
          textoD2: "Victor. <strong>(Ve hasta el semáforo y dale esto a Víctor)</strong>",
          name: "ice",
           tamano1:28,
           tamano2:39
        },
        {
          lista1: ["to"],

          textoA: "5. I want to run",

          textoD:
            "the top of the hill. <strong>(Quiero correr hasta la cima de la colina)</strong>",
          name: "ic",
           tamano:53
        },
        {
          lista1: ["to"],

          textoA: "6. Please, don’t tell me what",

          textoD: "do!<strong> (Por favor, no me digas qué hacer)</strong>",
          name: "ic",
           tamano:49
        },
        {
          lista1: ["to"],

          textoA: "7. I have bought this present to give it",

          textoD: "her. <strong>(He comprador este regalo para dárselo a ella)</strong>",
          name: "ic",
           tamano:62
        },
        {
          lista1: ["to"],

          textoA: "8. I would love to drive",

          textoD: "the desert. <strong>(Me encantaría conducir hasta el) </strong> ",
          name: "ic",
           tamano:49
        },
        {
          lista1: ["to"],

          textoA: "9. I am doing this",

          textoD:
            "help people in need.<strong> (Estoy haciendo esto para ayudar a las personas en necesidad)</strong>",
          name: "ic",
           tamano:70
        },
      ],

      cuestionario1Pag43: {
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
            A: 1,
            B: 1,
            C: 2,
            D: 1,
            complejo1: { lista: ["What do you do?"], tamano: 25 },
            E: "¿Qué haces? ",
          },
          {
            A: 1,
            B: 3,
            C: 2,
            D: 3,
            complejo1: { lista: ["What did you say?"], tamano: 25 },
            E: "¿Qué dijiste?",
          },
          {
            A: 5,
            B: 4,
            C: 2,
            D: 7,
            complejo1: { lista: ["When will you go?"], tamano: 25 },
            E: "¿Cuándo irás?",
          },
          {
            A: 2,
            B: 2,
            C: 3,
            D: 4,
            complejo1: { lista: ["Where does she live?"], tamano: 25 },
            E: "¿Dónde vive ella?",
          },
          {
            A: 3,
            B: 3,
            C: 2,
            D: 7,
            complejo1: { lista: ["Why did you go?"], tamano: 25 },
            E: "¿Por qué fuiste?",
          },
          {
            A: 5,
            B: 3,
            C: 6,
            D: 7,
            complejo1: { lista: ["When did we go?"], tamano: 25 },
            E: "¿Cuándo fuimos?",
          },
          {
            A: 4,
            B: 1,
            C: 2,
            D: 5,
            complejo1: { lista: ["How do you feel?"], tamano: 25 },
            E: "¿Cómo te sientes?",
          },
          {
            A: 1,
            B: 6,
            C: 2,
            D: 1,
            complejo1: { lista: ["What would you do?"], tamano: 25 },
            E: "¿Qué harías?",
          },
          {
            A: 2,
            B: 1,
            C: 2,
            D: 6,
            complejo1: { lista: ["Where do you work?"], tamano: 25 },
            E: "¿Dónde trabajas?",
          },
          {
            A: 1,
            B: 2,
            C: 3,
            D: 2,
            complejo1: { lista: ["What does she have?"], tamano: 25 },
            E: "¿Qué tiene ella?",
          },
          {
            A: 4,
            B: 3,
            C: 7,
            D: 5,
            complejo1: { lista: ["How did they feel?"], tamano: 25 },
            E: "¿Cómo se sintierón ellos?",
          },
          {
            A: 1,
            B: 1,
            C: 1,
            D: 1,
            complejo1: { lista: ["What I do?"], tamano: 25 },
            E: "¿Qué hago?",
          },
          {
            A: 5,
            B: 4,
            C: 7,
            D: 6,
            complejo1: { lista: ["When will they work?"], tamano: 25 },
            E: "¿Cuándo ellos trabajarán?",
          },
          {
            A: 1,
            B: 2,
            C: 4,
            D: 2,
            complejo1: { lista: ["What does he have?"], tamano: 25 },
            E: "¿Qué tiene él?",
          },
          {
            A: 4,
            B: 4,
            C: 2,
            D: 7,
            complejo1: { lista: ["How will you go?"], tamano: 25 },
            E: "¿Cómo irás?",
          },
          {
            A: 5,
            B: 5,
            C: 7,
            D: 7,
            complejo1: { lista: ["When will they go?"], tamano: 25 },
            E: "¿Cuándo irían ellos?",
          },
          {
            A: 3,
            B: 3,
            C: 2,
            D: 7,
            complejo1: { lista: ["Why did you go?"], tamano: 25 },
            E: "¿Por qué fuiste?",
          },
          {
            A: 1,
            B: 2,
            C: 4,
            D: 2,
            complejo1: { lista: ["What does he have?"], tamano: 25 },
            E: "¿Qué tiene él?",
          },
          {
            A: 4,
            B: 1,
            C: 2,
            D: 5,
            complejo1: { lista: ["How do you feel?"], tamano: 25 },
            E: "¿Cómo te sientes?",
          },
          {
            A: 1,
            B: 5,
            C: 2,
            D: 1,
            complejo1: { lista: ["What would you do?"], tamano: 25 },
            E: "¿Qué harías?",
          },
          {
            A: 3,
            B: 1,
            C: 2,
            D: 6,
            complejo1: { lista: ["Why did you work?"], tamano: 25 },
            E: "¿por qué trabajaste?",
          },
        ],
      },

     
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

inputChecked {
  display: inline-flex;
}
</style>