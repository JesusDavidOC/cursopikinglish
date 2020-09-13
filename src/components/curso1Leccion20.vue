<template>
  <div>
    <div class="row">
      <h3 id="subTitulo">LAS 4 CUATRO FORMAS DEL VERBO</h3>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <listaIndex :tabla="tablaP79" />
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">EL TIEMPO DE LOS MODIFICADORES</h3>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <listaIndex :tabla="tablaP79P2" />
        <h3 style="text-align: justify">
          Has completado la primera parte de la lógica del inglés, felicitaciones
          por atender las clases y realizar todas las asignaciones. Lo invitamos a
          disfrutar de la segunda parte de la lógica del inglés y que continúes
          animado con el nuevo método de aprender inglés, esto es solo el
          comienzo y nos aseguraremos que la pasión por el inglés no se acabe.
        </h3>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">¿CÓMO DAR ORDENES EN INGLES?</h3>
    </div>

    <div class="row" v-for="(item,index) in tablaPrueba">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row" id="textoCompromiso">
        <div class="col-sm-12">
          <dt>
            <i class="fa fa-diamond"></i>
            <a style="text-align: justify" v-html="item.texto">{{item.texto}}</a>
          </dt>
        </div>
        <div class="row"></div>
        <div class="col-sm-12 row">
          <div
            class="col-sm-3"
            v-for="item2 in item.palabras"
            style="text-align:center;padding:0"
            v-if="index < 1"
          >
            <h3 v-html="item2">{{item2}}</h3>
          </div>
          <div v-else>
            <h3 v-html="item2">{{item2}}</h3>
          </div>
        </div>
      </div>
      <div class="col-sm-1"></div>
    </div>

    <div class="row">
      <h3 id="subTitulo">PRACTICE</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" id="text">
        <i class="fa fa-diamond" style="font-size: 1.5em;"></i>
        <a id="textPractice">Escribe la traducción al frente</a>
      </div>
    </div>

    <div class="row" v-for="(item, index) in preguntasCompletarP24.items">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <div :class="'col-sm-'+item.tamaño">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP24.nombre+index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
          />
        </div>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">COMPLETA LAS SIGUIENTES ORACIONES</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-1" v-for="item in palabrasP81">
        <p>{{item}}</p>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div class="col-sm-12 row" v-for="(item, index) in preguntasCompletarP81.items">
          <div :class="'col-sm-'+item.tamaño">
            <inputChecked
              :esperado="item.esperado"
              :name="preguntasCompletarP81.nombre+index"
              :conTexto="true"
              :textoA="item.textoA"
              :textoD="item.textoD"
            />
          </div>
        </div>
      </div>
    </div>


    <div class="row">
      <h3 id="subTitulo">TRADUCE</h3>
    </div>

    <div class="row">
      <div class="col-sm-6" v-for="item in palabrasP81P2">
        <h5>{{item}}</h5>
      </div>
    </div>


    <div class="row" v-for="(item, index) in preguntasCompletarP81P2.items">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <div :class="'col-sm-'+item.tamaño">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP81P2.nombre+index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
          />
        </div>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">COMPLETA LA TABLA</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <tablaTC :cuestionario="tablaP82" /> 
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
  components: {
    listaIndex,
    inputChecked,
    tablaTC,
  },
  data() {
    return {
      tablaP82: {
        fields: [
          { key: "AFIRMATIVA", label: "ORDEN AFIRMATIVA" ,thClass: "Yelow" },
          { key: "TRADUCCIÓN", thClass: "Red" },
          { key: "complejo1", label: "ORDEN NEGATIVA", thClass: "Blue" },
          { key: "complejo2", label: "INVITACIÓN"},
        ],
        items: [
          {
            AFIRMATIVA: "Do that",
            TRADUCCIÓN: "Haz eso",
            complejo1: {
              lista: ["Don't do that"],
              textoA: "escriba ahora algo",
              textoD: "abr",
              tamano: 30,
            },
            complejo2: {
              lista: ["Let's do that"],
              textoA: "escriba ahora algo",
              textoD: "abr",
              tamano: 30,
            },
          },
          {
            AFIRMATIVA: "Do that",
            TRADUCCIÓN: "Haz eso",
            complejo1: {
              lista: ["Don't do that"],
              textoA: "escriba ahora algo",
              textoD: "abr",
              tamano: 30,
            },
            complejo2: {
              lista: ["Let's do that"],
              textoA: "escriba ahora algo",
              textoD: "abr",
              tamano: 30,
            },
          },
          {
            AFIRMATIVA: "Do that",
            TRADUCCIÓN: "Haz eso",
            complejo1: {
              lista: ["Don't do that"],
              textoA: "escriba ahora algo",
              textoD: "abr",
              tamano: 30,
            },
            complejo2: {
              lista: ["Let's do that"],
              textoA: "escriba ahora algo",
              textoD: "abr",
              tamano: 30,
            },
          },
          {
            AFIRMATIVA: "Do that",
            TRADUCCIÓN: "Haz eso",
            complejo1: {
              lista: ["Don't do that"],
              textoA: "escriba ahora algo",
              textoD: "abr",
              tamano: 30,
            },
            complejo2: {
              lista: ["Let's do that"],
              textoA: "escriba ahora algo",
              textoD: "abr",
              tamano: 30,
            },
          },
          {
            AFIRMATIVA: "Do that",
            TRADUCCIÓN: "Haz eso",
            complejo1: {
              lista: ["Don't do that"],
              textoA: "escriba ahora algo",
              textoD: "abr",
              tamano: 30,
            },
            complejo2: {
              lista: ["Let's do that"],
              textoA: "escriba ahora algo",
              textoD: "abr",
              tamano: 30,
            },
          },
          {
            AFIRMATIVA: "Do that",
            TRADUCCIÓN: "Haz eso",
            complejo1: {
              lista: ["Don't do that"],
              textoA: "escriba ahora algo",
              textoD: "abr",
              tamano: 30,
            },
            complejo2: {
              lista: ["Let's do that"],
              textoA: "escriba ahora algo",
              textoD: "abr",
              tamano: 30,
            },
          },
        ],
      },
      palabrasP81: [
        "STOP",
        "PLAY",
        "EAT",
        "SLEEP",
        "SING",
        "THINK OF",
        "TALK TO",
        "STUDY",
      ],
      palabrasP81P2: [
        "- Don't talk to her",
        "- Go quickly",
        "- Calm down",
        "- Don't smoke in here",
        "- Don't say that",
        "- Let's go",
        "- Don't put off for tomorrow what you can do today",
        "- Call me back tomorrow morning",
        "- Read",
        "- Believe me",
        "- Let's go for a walk",
        "- Don't write",
      ],
      tablaPrueba: [
        {
          texto:
            "Solo es necesario usar el verbo para ordenar una acción a la persona con quien se habla. No se usa subjeto.",
          palabras: [
            "<span class='colorLetraRojo'>Go:</span> Vete",
            "Look at me: Mírame",
            "Listen: Escucha",
            "Sit down: Siéntate",
          ],
        },
        {
          texto:
            "Si queremos decir no a esas acciones anteriores solo basta con agregar la negación DON´T antes del verbo.",
          palabras: [
            "<span class='colorLetraRojo'>Don’t</span>go: No vayas |",
            "<span class='colorLetraRojo'>Don’t</span>look at me: No me mires |",
            "<span class='colorLetraRojo'>Don’t</span>listen: No escuches |",
          ],
        },
        {
          texto:
            "Si queremos una acción compartida; es decir que la persona con quien hablas haga lo mismo que tú, solo usa LET´S al iniciar la acción seguida del verbo. Esta palabra LET´S hace que un verbo termine en MOS.",
          palabras: [
            "<span class='colorLetraRojo'>Let's</span> go: Vamos |",
            "<span class='colorLetraRojo'>Let's</span> eat: Comamos|",
            "<span class='colorLetraRojo'>Let's</span> sit down: Sentémonos|",
          ],
        },
      ],
      tablaP79: {
        fields: [
          { key: "html", label: "THE MAGIC NUMBER" },
          { key: "present", label: "PRESENT", thClass: "Yelow" },
          { key: "presentsE", label: "PRESENTS-ES-IES", thClass: "Yelow" },
          { key: "past", label: "PAST", thClass: "Red" },
          { key: "participle", label: "PARTICIPLE", thClass: "Blue" },
          { key: "progresive", label: "PROGRESIVE", thClass: "Blue2" },
        ],
        bordered: true,
        items: [
          {
            html:
              "<p style='font-size:18px' class='text-left'>Oraciones en presente</p>",
            present: "Go",
          },
          {
            html:
              "<p style='font-size:18px' class='text-left'>Oraciones en presente afirmativo con <strong>she, he, it</strong></p>",
            presentsE: "Goes",
          },
          {
            html:
              "<p style='font-size:18px' class='text-left' >Oraciones con modificadores <strong> Do-Does-Did-Will-Would </strong> </p>",
            present: "Go",
          },
          {
            html:
              "<p style='font-size:18px' class='text-left' >Oraciones con S.P.V <strong> Can-Could-Should-Must</strong> </p>",
            present: "Go",
          },
          {
            html:
              "<p style='font-size:18px' class='text-left' >Oraciones en pasado afirmativo</p>",
            past: "Went",
          },
          {
            html:
              "<p style='font-size:18px' class='text-left' >Oraciones con S.P.V <strong> Have-Has-Had </strong></p>",
            participle: "Gone",
          },
          {
            html:
              "<p style='font-size:18px' class='text-left' >Oraciones con S.P.V <strong> Is-Am-Are-Was-Were </strong></p>",
            progresive: "Going",
          },
        ],
      },
      tablaP79P2: {
        fields: [
          { key: "html", label: "MODIFICADORES" },
          { key: "present", label: "PRESENT", thClass: "Yelow" },
          { key: "present2", label: "PRESENT", thClass: "Red" },
          { key: "past", label: "PAST", thClass: "Blue" },
          { key: "futuro", label: "FUTURO", thClass: "Blue2" },
          { key: "ria", label: "'RÍA'", thClass: "White" },
        ],
        bordered: true,
        items: [
          {
            html:
              "<p style='font-size:18px' class='text-left'> <strong> Do </strong> you work</p>",
            present: "¿Trabajas?",
          },
          {
            html:
              "<p style='font-size:18px' class='text-left'><strong>Does</strong> she work?</p>",
            present2: "¿Ella trabaja?",
          },
          {
            html:
              "<p style='font-size:18px' class='text-left'><strong> Did </strong> you work? </p>",
            past: "¿Trabajaste?",
          },
          {
            html:
              "<p style='font-size:18px' class='text-left' ><strong> Will </strong> you work? </p>",
            futuro: "¿Trabajarás?",
          },
          {
            html:
              "<p style='font-size:18px' class='text-left' > <strong> Would </strong> you work? </p>",
            ria: "¿Trabajarías?",
          },
        ],
      },
      preguntasCompletarP24: {
        nombre: "preguntasCompletarP24",
        items: [
          {
            esperado: ["Go"],
            textoA: "1. ve",
            textoD: "",
            tamaño: 3,
          },
          {
            esperado: ["dont go"],
            textoA: "2. no vayas ",
            textoD: "",
            tamaño: 4,
          },
          {
            esperado: ["let's go"],
            textoA: "3. vamos",
            textoD: "",
            tamaño: 4,
          },
          {
            esperado: ["let's not go"],
            textoA: "4. No vayamos ",
            textoD: "",
            tamaño: 4,
          },
          {
            esperado: ["dont do it"],
            textoA: "5. No lo hagas",
            textoD: "",
            tamaño: 4,
          },
          {
            esperado: ["do it"],
            textoA: "6. Hazlo",
            textoD: "",
            tamaño: 3,
          },
          {
            esperado: ["let's do it"],
            textoA: "7. Hagámoslo",
            textoD: "",
            tamaño: 4,
          },
          {
            esperado: ["call me"],
            textoA: "8. Llámame",
            textoD: "",
            tamaño: 4,
          },
          {
            esperado: ["dont call me"],
            textoA: "9. No me llames",
            textoD: "",
            tamaño: 5,
          },
          {
            esperado: ["let's call her"],
            textoA: "10. Llamémosla",
            textoD: "",
            tamaño: 5,
          },
          {
            esperado: ["close the door"],
            textoA: "11. cierra la puerta",
            textoD: "",
            tamaño: 5,
          },
          {
            esperado: ["dont close the door"],
            textoA: "12. No cierres la puerta",
            textoD: "",
            tamaño: 6,
          },
          {
            esperado: ["listen to music"],
            textoA: "13. Escucha la música",
            textoD: "",
            tamaño: 6,
          },
          {
            esperado: ["dont listen to me"],
            textoA: "14 no me escuches",
            textoD: "",
            tamaño: 5,
          },
        ],
      },
      preguntasCompletarP81: {
        nombre: "preguntasCompletarP81",
        items: [
          {
            esperado: ["stop"],
            textoA: "1. Hey",
            textoD: ", please! - Hola detente por favor",
            tamaño: 8,
          },
          {
            esperado: ["play"],
            textoA: "2. let's",
            textoD: "cards to night! -   Juguemos cartas esta noche",
            tamaño: 8,
          },
          {
            esperado: ["eat"],
            textoA: "3. don't",
            textoD: "that, it´s expired! -  No te comas eso, está vencido",
            tamaño: 8,
          },
          {
            esperado: ["sleep"],
            textoA: "4. ",
            textoD:
              "well; tomorrow it will be a long day! - Duerme bien, mañana será un largo día",
            tamaño: 10,
          },
          {
            esperado: ["study"],
            textoA: "5. let's",
            textoD: "for the test! - Estudiemos para el examen",
            tamaño: 8,
          },
          {
            esperado: ["sing"],
            textoA: "6. Please, don't",
            textoD: "out loud - no cantes tan alto",
            tamaño: 8,
          },
          {
            esperado: ["think of"],
            textoA: "7. ",
            textoD: "me honey! - Piensa en mi cariño",
            tamaño: 8,
          },
          {
            esperado: ["talk to"],
            textoA: "8. don't",
            textoD: "her - No hables con ella",
            tamaño: 8,
          },
          
        ],
      },
      preguntasCompletarP81P2: {
        nombre: "preguntasCompletarP81P2",
        items: [
          {
            esperado: ["go quickly"],
            textoA: "1. Ve rápido",
            textoD: "",
            tamaño: 4,
          },
          {
            esperado: ["don't say that"],
            textoA: "2. No digas eso",
            textoD: "",
            tamaño: 5,
          },
          {
            esperado: ["let's go"],
            textoA: "3. Vamos",
            textoD: "",
            tamaño: 4,
          },
          {
            esperado: ["let's go for a walk"],
            textoA: "4. Vamos a dar un paseo",
            textoD: "",
            tamaño: 6,
          },
          {
            esperado: ["don't write"],
            textoA: "5. No escribas",
            textoD: "",
            tamaño: 4,
          },
          {
            esperado: ["read"],
            textoA: "6. Lee",
            textoD: "",
            tamaño: 3,
          },
          {
            esperado: ["don't smoke in here"],
            textoA: "7. No fumes aquí adentro",
            textoD: "",
            tamaño: 6,
          },
          {
            esperado: ["call me back tomorrow morning"],
            textoA: "8. Devuélveme la llamada mañana en la mañana",
            textoD: "",
            tamaño: 10,
          },
          {
            esperado: ["calm down"],
            textoA: "9. Cálmate",
            textoD: "",
            tamaño: 4,
          },
          {
            esperado: ["don’t put off for tomorrow what you can do today"],
            textoA: "9. No dejes para mañana lo que puedas hacer hoy",
            textoD: "",
            tamaño: 11,
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
</style>
