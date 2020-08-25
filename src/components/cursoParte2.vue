<template>
  <div class="row">
    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-2">
        <div class="col-sm-7" id="numeroMagico" style="background: yellow;">2</div>
        <h3 style="margin-top:0.4em;">Types Of Verbs</h3>
        <listaIndex :tabla="$data.tablasNumeroMagico[0]" />
      </div>
      <div class="col-sm-2">
        <div class="col-sm-7" id="numeroMagico" style="background: red;">4</div>
        <h3 style="margin-top:0.4em;">Spelling Forms</h3>
        <listaIndex :tabla="$data.tablasNumeroMagico[1]" />
      </div>
      <div class="col-sm-2">
        <div class="col-sm-7" id="numeroMagico" style="background: royalblue;">5</div>
        <h3 style="margin-top:0.4em;">Tense Modifiers</h3>
        <listaIndex :tabla="$data.tablasNumeroMagico[2]" />
      </div>
      <div class="col-sm-2">
        <div class="col-sm-7" id="numeroMagico" style="background:cadetblue">12</div>
        <h4 style="margin-top:0.4em;">Super Power Verbs</h4>
        <listaIndex :tabla="$data.tablasNumeroMagico[3]" />
      </div>
    </div>
    <div class="row">

    </div>
  </div>
</template>

<script>
import posiblesRespuestasTabla from "./posiblesRespuestasTabla";
import opcionMultiple from "./opcionMultiple";
import listaIndex from "./listaIndex";
import inputChecked from "./inputChecked";
export default {
  components: {
    opcionMultiple,
    listaIndex,
    inputChecked,
    posiblesRespuestasTabla,
  },
  data() {
    return {
      tablasNumeroMagico: [
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
            "Have",
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
    };
  },
};
</script>>

<style scoped>
    #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

#curso{
  padding-left: 1em;
}
 .row {
  width: 100%;
  margin: 0;
}
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

#numeroMagico {
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