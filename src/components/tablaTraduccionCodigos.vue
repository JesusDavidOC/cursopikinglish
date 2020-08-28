<template>
  <div >
    <b-table
      id="cuestionario"
      small
      :fields="this.cuestionario.fields"
      :items="this.cuestionario.items"
      responsive="sm"
      :bordered="true"
    >
      <template v-slot:cell(complejo1)="row" id="hola">
        <inputChecked :style="'width:'+row.item.complejo1.tamano+'em;'"
          :resuelto="$props.inglesR"
          :esperado="row.item.complejo1.lista"
          :conTexto="true"
          :textoA="row.item.complejo1.textoA"
          :textoD="row.item.complejo1.textoD"
        />
      </template>
      <template v-slot:cell(complejo2)="row" id="hola">
        <inputChecked :style="'width:'+row.item.complejo2.tamano+'em;'"
          :resuelto="$props.inglesR"
          :esperado="row.item.complejo2.lista"
          :conTexto="true"
          :textoA="row.item.complejo2.textoA"
          :textoD="row.item.complejo2.textoD"
        />
      </template>

      <template v-slot:cell(complejo3)="row" id="hola">
        <inputChecked :style="'width:'+row.item.complejo3.tamano+'em;'"
          :resuelto="$props.inglesR"
          :esperado="row.item.complejo3.lista"
          :conTexto="true"
          :textoA="row.item.complejo3.textoA"
          :textoD="row.item.complejo3.textoD"
        />
      </template>

      <template v-slot:cell(complejo4)="row" id="hola">
        <inputChecked :style="'width:'+row.item.complejo4.tamano+'em;'"
          :resuelto="$props.inglesR"
          :esperado="row.item.complejo4.lista"
          :conTexto="true"
          :textoA="row.item.complejo4.textoA"
          :textoD="row.item.complejo4.textoD"
        />
      </template>

      <template v-slot:cell(TRADUCCION_ESPAÑOL)="row">
        <inputChecked :resuelto="$props.espanolR" :esperado="row.item.TRADUCCION_ESPAÑOL" />
      </template>
    </b-table>
  </div>
</template>


<script>
import inputChecked from "./inputChecked";

export default {
  components: {
    inputChecked,
  },
  props: {
    cuestionario: Object,
    espanolR: Boolean,
    inglesR: Boolean,
  },
  mounted() {},
};
</script>


<style scoped>

</style>