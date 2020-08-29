<template>
  <div>
    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8" id="cuadroTexto">
        <h3>Recuerde que un verbo se usa su<span class="colorLetraRojo">forma presente lógicamente en presente </span> o después de un auxiliar y siempre tenga en cuenta que los auxiliares sirven para negar o preguntar.</h3>
      </div>
      <div class="col-sm-2"></div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-7 row">
        <div class="col-sm-3" v-for="item in tablasContenido1P27">
          <listaIndex :tabla="item" />
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-9">
        <tablaTC
          class="overflow-auto"
          :cuestionario="$data.cuestionario1P27"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <div class="col-sm-1"></div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-7 row">
        <div class="col-sm-3" v-for="item in tablasContenido2P27">
          <listaIndex :tabla="item" />
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-7">
        <tablaTC
          class="overflow-auto"
          :cuestionario="cuestionario2P27"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <div class="col-sm-1"></div>
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
  data() {
    return {
        cuestionario2P27: {
        fields: [
          { key: "A", thClass: "Blue" },
          { key: "B", thClass: "Red" },
          { key: "C", thClass: "Yelow" },
          { key: "complejo1", label: "ENGLISH" },
          { key: "ESPANOL", label: "SPANISH" },
        ],
        items: [
          {
            A: 1,
            B: 1,
            C: 1,  
            complejo1: { lista: ["Do you go?"] },
            ESPANOL: "¿Tú vas?",
          },
          {
            A: 2,
            B: 2,
            C: 1,
            complejo1: { lista: ["Does she go?"] },
            ESPANOL: "¿Ella va?",
          },
          {
            A: 3,
            B: 2,
            C: 1,
            complejo1: { lista: ["Did she go?"] },
            ESPANOL: "¿Ella fue?",
          },
          {
            A: 4,
            B: 1,
            C: 1,
            complejo1: { lista: ["Will you go?"] },
            ESPANOL: "¿Tú irás?",
          },
          {
            A: 5,
            B: 2,
            C: 1,
            complejo1: { lista: ["Would she go?"] },
            ESPANOL: "¿Ella iría?",
          },
        ],
      },
      tablasContenido2P27: [
        {
          bordered: true,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            "#",
            // A column that needs custom formatting
            { key: "A", thClass: "Blue" },
          ],
          items: [
            { A: "Do" },
            { A: "Does" },
            { A: "Did" },
            { A: "Will" },
            { A: "Would" },
          ],
        },

        {
          bordered: true,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            "#",
            // A column that needs custom formatting
            { key: "B", thClass: "Red" },
          ],
          items: [{ B: "You" }, { B: "She" }],
        },
        {
          bordered: true,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            "#",
            // A column that needs custom formatting
            { key: "C", thClass: "Yelow" },
          ],
          items: [{ C: "go ...?" }],
        },
      ],
      cuestionario1P27: {
        fields: [
          { key: "A", thClass: "Blue" },
          { key: "B", thClass: "Red" },
          { key: "C", thClass: "Yelow" },
          { key: "D", thClass: "Green" },
          { key: "complejo1", label: "ENGLISH" },
          { key: "ESPANOL", label: "SPANISH" },
        ],
        items: [
          {
            A: 1,
            B: 1,
            C: 1,
            D: 2,
            complejo1: { lista: ["I don´t have a friend"] },
            ESPANOL: "Yo no tengo un amigo",
          },
          {
            A: 2,
            B: 2,
            C: 1,
            D: 1,
            complejo1: { lista: ["She doesn´t have that"] },
            ESPANOL: "Ella no tiene eso",
          },
          {
            A: 1,
            B: 3,
            C: 2,
            D: 1,
            complejo1: { lista: ["I didn´t do that"] },
            ESPANOL: "Yo no hice eso",
          },
          {
            A: 2,
            B: 4,
            C: 2,
            D: 1,
            complejo1: { lista: ["She won´t do that"] },
            ESPANOL: "Ella no hará eso",
          },
          {
            A: 1,
            B: 5,
            C: 2,
            D: 1,
            complejo1: { lista: ["I wouldn´t do that"] },
            ESPANOL: "Yo no haría eso",
          },
        ],
      },
      tablasContenido1P27: [
        {
          bordered: true,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            "#",
            // A column that needs custom formatting
            { key: "A", thClass: "Blue" },
          ],
          items: [{ A: "I" }, { A: "SHE" }],
        },

        {
          bordered: true,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            "#",
            // A column that needs custom formatting
            { key: "B", thClass: "Red" },
          ],
          items: [
            { B: "Don´t" },
            { B: "Doesn´t" },
            { B: "Didn´t" },
            { B: "Won´t" },
            { B: "Wouldn´t" },
          ],
        },
        {
          bordered: true,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            "#",
            // A column that needs custom formatting
            { key: "C", thClass: "Yelow" },
          ],
          items: [{ C: "Have" }, { C: "Do" }],
        },
        {
          bordered: true,
          camposInput: false,
          fields: [
            // A virtual column that doesn't exist in items
            { key: "#" },
            ,
            // A column that needs custom formatting
            { key: "D", thClass: "Green" },
          ],
          items: [{ D: "That" }, { D: "A friend" }],
        },
      ],
    };
  },
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