<template>
  <div>
    <div class="row" style="margin-top:-3em;">
      <div class="col-sm-1"></div>
      <div class="col-sm-12" id="subTitulo">
        <h3>EXAMEN DE COMPRENSIÓN</h3>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6" id="text">
        <opcionMultiple
          :options="$data.cuestionarioP18"
          :rEsperadas="$data.respuestasCuestionarioP18"
          @respuestas="$data.mensajeRespuestasP18 = $event"
        />
      </div>
      <b-modal ref="my-modalP18" hide-footer title="RESULTADO">{{mensajeRespuestasP18 }}</b-modal>
      <div class="col-sm-1"></div>
    </div>   
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-3">
        <b-button variant="primary" @click="showModal('my-modalP18')">VERIFICAR PREGUNTAS</b-button>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6" style="text-align:left;">
        <legend
          id="5__BV_label_"
          tabindex="-1"
          class="bv-no-focus-ring col-form-label pt-0 col-form-label-lg labelPregunta"
        >16. Escribe la forma del verbo que se usa con los siguientes verbos con poder.</legend>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row" id="titulo" style="margin:0;">
        <div class="col-sm-3">
          <h3>PRESENTE</h3>
        </div>
        <div class="col-sm-3">
          <h3>PASADO</h3>
        </div>
        <div class="col-sm-3">
          <h3>PARTICIPIO</h3>
        </div>
        <div class="col-sm-3">
          <h3>PROGRESIVO</h3>
        </div>
      </div>
    </div>
    <div class="row" style="margin:0em;">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div
          class="col-sm-1"
          v-for="(item, index) in palabrasListaP18.fields"
          style="margin:0; padding:0;"
        >
          <listaIndex :tabla="{bordered:true, fields: [item]}" />
        </div>
      </div>
    </div>
    <div class="row" style="margin-top:-1.5em;">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div class="col-sm-3" style="padding:0;">
          <inputChecked :esperado="['participio']" :resuelto="false" />
        </div>
        <div class="col-sm-5" style="padding:0;">
          <inputChecked :esperado="['progresivo']" :resuelto="false" />
        </div>
        <div class="col-sm-4" style="padding:0;">
          <inputChecked :esperado="['presente']" :resuelto="false" />
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6" style="text-align:left;">
        <legend
          id="5__BV_label_"
          tabindex="-1"
          class="bv-no-focus-ring col-form-label pt-0 col-form-label-lg labelPregunta"
        >17. Completa el número mágico.</legend>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-2">
        <div class="col-sm-7" id="numeroMagico2" >2</div>
        <h3 style="margin-top:0.4em;">Types Of Verbs</h3>
        <listaIndex :tabla="$data.tablasNumeroMagicoP19[0]" />
      </div>
      <div class="col-sm-2">
        <div class="col-sm-7" id="numeroMagico4" >4</div>
        <h3 style="margin-top:0.4em;">Spelling Forms</h3>
        <listaIndex :tabla="$data.tablasNumeroMagicoP19[1]" />
      </div>
      <div class="col-sm-2">
        <div class="col-sm-7" id="numeroMagico5" >5</div>
        <h3 style="margin-top:0.4em;">Auxiliares</h3>
        <listaIndex :tabla="$data.tablasNumeroMagicoP19[2]" />
      </div>
      <div class="col-sm-2">
        <div class="col-sm-7" id="numeroMagico12">12</div>
        <h4 style="margin-top:0.4em;">Super Power Verbs</h4>
        <listaIndex :tabla="$data.tablasNumeroMagicoP19[3]" />
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6" style="text-align:left;">
        <legend
          id="5__BV_label_"
          tabindex="-1"
          class="bv-no-focus-ring col-form-label pt-0 col-form-label-lg labelPregunta"
        >18. Escribe los auxiliares y verbos con poder debajo de cada forma.</legend>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <div
          class="col-sm-3"
          v-for="item in $data.tablasTiempoPreguntaP19"
          style="margin:0; padding:0;"
        >
          <listaIndex :tabla="item" />
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10 row">
        <ul id="textoCompromiso">
          <dt v-for="(item, index) in $data.listadoP20">
            <i class="fa fa-diamond"></i>
            <a v-html="item">{{ item }}</a>            
          </dt>
        </ul>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"> </div>
      <div class="col-sm-10">      
        <img src="/cursos/curso1/leccion3/imagenes/pag20.PNG" />
      </div>
    </div>
  </div>
</template>


<script>
import posiblesRespuestasTabla from "./posiblesRespuestasTabla";
import opcionMultiple from "./opcionMultiple";
import listaIndex from "./listaIndex";
import inputChecked from "./inputChecked";
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
  },
  data() {
    return {
        listadoP20: [
        "La forma presente de un verbo se usa con los auxiliares o después de los verbos con poder CAN, COULD, SHOULD y MUST.",
        "Los verbos regulares en su forma pasada o participio se les agrega ED.",
        "La forma participio siempre se usa con HAVE-HAS Y HAD.",
        "La forma progresiva de un verbo se usa después de IS, AM, ARE, WAS Y WERE",        
      ],
      tablasNumeroMagicoP19: [
        {
          refs: "tablasNumeroMagicoa",
          bordered: false,
          camposInput: true,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "Z", thClass: "noHead" },
          ],
          items: ["Regulars", "Irregulars"],
        },
        {
          refs: "tablasNumeroMagicob",
          bordered: false,
          camposInput: true,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "Z", thClass: "noHead" },
          ],
          items: ["Present", "Past", "Participle", "Progessive"],
        },
        {
          refs: "tablasNumeroMagicoc",
          bordered: false,
          camposInput: true,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "Z", thClass: "noHead" },
          ],
          items: ["Do", "Does", "Did", "Will", "Would"],
        },
        {
          refs: "tablasNumeroMagicod",
          bordered: false,
          camposInput: true,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "Z", thClass: "noHead" },
          ],
          items: [
            "Has",
            "Had",
            "Is",
            "Am",
            "Are",
            "Was",
            "Were",
            "Can",
            "Could",
            "Should",
            "Must",
          ],
        },
      ],
      tablasTiempoPreguntaP19: [
        {
          refs: "tablasTiempoPreguntaP15a",
          bordered: false,
          camposInput: true,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "Z", label: "PRESENT", thClass: "colorLetraRojo" },
          ],
          items: [
            "Do",
            "Does",
            "Did",
            "Will",
            "Would",
            "Can",
            "Could",
            "Should",
            "Must",
          ],
        },
        {
          bordered: false,
          camposInput: true,
          refs: "tablasTiempoPreguntaP15b",
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            { key: "Z", label: "PAST", thClass: "colorLetraRojo" },
          ],
          items: ["Oraciones Afirmativas"],
        },
        {
          refs: "tablasTiempoPreguntaP15c",
          bordered: false,
          camposInput: true,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              label: "PARTICIPLE " + "'ado-ido'",
              thClass: "colorLetraRojo",
            },
          ],
          items: ["Have", "Has", "Had"],
        },
        {
          refs: "tablasTiempoPreguntaP15d",
          bordered: false,
          camposInput: true,
          fields: [
            // A virtual column that doesn't exist in items
            // A column that needs custom formatting
            {
              key: "Z",
              label: "PROGRESSIVE \n 'ando-endo'",
              thClass: "colorLetraRojo",
            },
          ],
          items: ["Is", "Am", "Are", "Was", "Were"],
        },
      ],
      palabrasListaP18: {
        fields: [
          "Have",
          "Has",
          "Had",
          "Is",
          "Are",
          "Am",
          "Was",
          "Were",
          "Can",
          "Could",
          "Should",
          "Must",
        ],
      },
      mensajeRespuestasP18: "Complete las preguntas",
      respuestasCuestionarioP18: [
        "A",
        "A",
        "A",
        "A",
        "B",
        "A",
        "B",
        "B",
        "A",
        "A",
        "B",
        "B",
        "B",
        "A",
        "B",
      ],
      cuestionarioP18: [
        {
          respuesta: "",
          pregunta: "1. ¿Cuál es la tercera forma de un verbo?",
          options: [
            {
              text: "A) Participio.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Presente.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "2. ¿Qué se le agrega a un verbo regular en pasado y participio?",
          options: [
            {
              text: "A) Ed.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Ing.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "3. ¿Para qué sirve un auxiliar? ",
          options: [
            {
              text: "A) Para negar y preguntar.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Para afirmar.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "4. ¿Por qué se le llaman verbos con super poderes?",
          options: [
            {
              text: "A) Por que usan auxiliares.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Porque se pueden negar solos.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "5. ¿Cuáles verbos con super poder se usan en la forma participio?",
          options: [
            {
              text: "A) Can y could.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Have, has y had.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "6. ¿En qué forma se usa el verbo si hay un auxiliar?",
          options: [
            {
              text: "A) Presente.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Pasado.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "7. Para usar un verbo en su forma pasada la oración debe ser:",
          options: [
            {
              text: "A) Negativa.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Afirmativa.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "8. ¿En que termina un verbo después del auxiliar WOULD en español?",
          options: [
            {
              text: "A) Ré.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Ría.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "9. ¿Qué se usa para negar o preguntar?",
          options: [
            {
              text: "A) Un auxiliar.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Solo el verbo.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "10. ¿Cuál es el auxiliar que se usa para hacer preguntas en pasado?",
          options: [
            {
              text: "A) Did.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Do.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "11. ¿Cuál es el auxiliar para preguntar en presente con she he e it? ",
          options: [
            {
              text: "A) Do.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Does.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "12. ¿Qué forma del verbo se usa después de los verbos con poder HAVE, HAS Y HAD?",
          options: [
            {
              text: "A) Pasado.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Participio.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "13. ¿Qué se le agrega a un verbo regular en su forma pasado o participio?",
          options: [
            {
              text: "A) Ing.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Ed.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "14. ¿Cuáles verbos con super poder se usa en la forma progresiva?",
          options: [
            {
              text: "A) Is, am, are, was, were.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Should.",
              value: "B",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "15. ¿Después de CAN, COULD, SHOULD Y MUST en qué forma se usa el verbo?",
          options: [
            {
              text: "A) Pasado.",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Presente.",
              value: "B",
              disabled: false,
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
/deep/.labelPregunta{
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

#numeroMagico2, #numeroMagico4,#numeroMagico5, #numeroMagico12 {
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
#numeroMagico2{
    background: yellow;
}

#numeroMagico4{
    background: red;
}
#numeroMagico5{
    background: royalblue;
}
#numeroMagico12{
    background:cadetblue
}

#text,
#inputText {
  text-align: left;
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