<template>
  <div>
    <div class="row">
      <div class="col-sm-1"></div>
      <h3 class="titulo">AUXILIARES NEGATIVOS</h3>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <p
        class="parrafoBlack"
      >Recuerde que un verbo se usa en su forma presente por lógica en presente o después de un auxiliar.</p>
    </div>
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

inputChecked {
  display: inline-flex;
}
</style>