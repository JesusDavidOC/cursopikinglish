<template>
  <div>
    <h3 class="titulo">FORMA PRESENTE CON AUXILIARES NEGATIVOS</h3>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-11 row">
        <div class="col-sm-2 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaAPag38" />
        </div>
        <div class="col-sm-2 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaBPag38" />
        </div>
        <div class="col-sm-2 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaCPag38" />
        </div>
        <div class="col-sm-2 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaDPag38" />
        </div>
      </div>
    </div>

    <br />

    <div class="row">
      <i class="fa fa-diamond marginn-left"></i>

      <p class="parrafoBlack marginn-left">
        &nbsp;
        <b>Un verbo también se usa en su forma presente después de un auxiliar.</b>
      </p>
      <br />
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-11 row">
        <div class="col-sm-4 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaAPag33" />
        </div>
        <div class="col-sm-4 parrafoBlack" id="tabla">
          <listaIndex :tabla="$data.tablaBPag33" />
        </div>
      </div>
    </div>
    <img src="/cursos/curso1/leccion8/imagenes/tablaPag38.png" />

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="subTitulo parrafoBlack">Existen cinco maneras de preguntar y negar en inglés</div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-9">
        <tablaTC
          class="overflow-auto"
          :cuestionario="tabla2P29"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
      <div class="col-sm-1"></div>
    </div>

    <div class="row">
      <i class="fa fa-diamond marginn-left"></i>

      <p class="parrafoBlack marginn-left Subrayado">
        &nbsp;
        <b>Ubique el auxiliar negativo en las siguientes oraciones.</b>
      </p>
      <br />
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-8 row">
        <div
          v-for="(item, index) in frases2PAg37"
          :class=" ' row col-sm-'+item.tamano+4"
          style="margin-bottom:0.5em;"
        >
          <inputChecked
            :esperado="item.esperado"
            :resuelto="false"
            :name="'P21-'+index"
            :textoA="item.textoA"
            :textoD="item.textoD"
            :conTexto="true"
          />
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import posiblesRespuestasTabla from "./posiblesRespuestasTabla";
import listaIndex from "./listaIndex";
import inputChecked from "./inputChecked";
import tablaTraduccionCodigos from "./tablaTraduccionCodigos";
import tablaTraduccionCodigosDos from "./tablaTraduccionCodigosDos";
import tablaTC from "./tablaTraduccionCodigos";
export default {
  components: {
    listaIndex,
    inputChecked,
    tablaTraduccionCodigos,
    tablaTraduccionCodigosDos,
    posiblesRespuestasTabla,
    tablaTC,
  },
  data() {
    return {
      tablaAPag38: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "A", thClass: "Yellow Subrayado", label: "PRESENT" },
        ],

        items: [],
      },

      tablaBPag38: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "PAST", thClass: "Subrayado" },
        ],
        items: [],
      },

      tablaCPag38: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "PARTICIPE", thClass: " Subrayado" },
        ],
        items: [],
      },

      tablaDPag38: {
        bordered: true,

        fields: [
          // A virtual column that doesn't exist in items

          // A column that needs custom formatting
          { key: "PROGRESSIVE", thClass: " Subrayado" },
        ],
        items: [],
      },

      cuestionario1Pag36: {
        fields: [
          {
            key: "A",
            thClass: "Yellow parrafoBlack",
            label: "Verbo en presente",
          },
          { key: "ENGLISH_PHRASE", label: "En tercera persona" },
          { key: "B", label: "Clase" },
          { key: "C", label: "Past and participle" },
        ],
        items: [
          {
            A: "I *Eat* pizza",
            B: "Irregular",
            C: "Ate – eaten",

            ENGLISH_PHRASE: ["She eats pizza"],
          },
        ],
      },

      tabla2P29: {
        fields: [
          { key: "Z", label: "1.", thClass: "noHead" },
          { key: "A", label: "A", thClass: "noHead" },
          { key: "complejo1", label: "A", thClass: "noHead" },
          { key: "B", label: "A", thClass: "noHead" },
          { key: "complejo2", label: "A", thClass: "noHead" },
        ],
        items: [
          {
            Z: "1.",
            A: "Do you eat?",
            complejo1: { lista: ["¿Tú comes?"], tamano: 18 },
            B: "I don't eat",
            complejo2: { lista: ["Yo no como"], tamano: 18 },
          },
          {
            Z: "2.",
            A: "Did you eat?",
            complejo1: { lista: ["¿Tú comiste?"], tamano: 18 },
            B: "I didn´t eat",
            complejo2: { lista: ["Yo no comí"], tamano: 18 },
          },
          {
            Z: "3.",
            A: "Will you eat?",
            complejo1: { lista: ["¿Tú comerás?"], tamano: 18 },
            B: "I won't eat",
            complejo2: { lista: ["Yo no comeré"], tamano: 18 },
          },
          {
            Z: "4.",
            A: "Would you eat?",
            complejo1: { lista: ["¿Tú comerías?"], tamano: 18 },
            B: "I wouldn't eat",
            complejo2: { lista: ["Yon no comería"], tamano: 18 },
          },
          {
            Z: "5",
            A: "Does she it?",
            complejo1: { lista: ["¿Ella come?"], tamano: 18 },
            B: "She doesn't eat",
            complejo2: { lista: ["Ella no come"], tamano: 18 },
          },
        ],
      },
      frases2PAg37: [
        {
          esperado: ["didn't"],
          textoA: "1. I ",
          tamano: 4,
          textoD: "understand. (Yo no entendí)",
        },

        {
          esperado: ["doesn't "],
          textoA: "2. She",
          tamano: 4,
          textoD: "live here. (Ella no vive aquí)",
        },
        {
          esperado: ["wont't"],
          textoA: "3. You",
          tamano: 4,
          textoD: "understand. (Tú no entenderías)",
        },
        {
          esperado: ["don't"],
          textoA: "4. I",
          tamano: 4,
          textoD: " care. (No me importa)",
        },
        {
          esperado: ["won't"],
          textoA: "5. They",
          tamano: 4,
          textoD: "say anything. (Ellos no dirán nada)",
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
</style>