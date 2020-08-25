<template>
  <div id="diiv" class="overflow-auto">
    <b-table
      id="cuestionario"
      small
      :fields="this.cuestionario.fields"
      :items="this.cuestionario.items"
      responsive="sm"
      :bordered="true"
    >
      <template v-slot:cell(ENGLISH_PHRASE)="row" id="hola">
        <inputChecked :resuelto="$props.inglesR" :esperado="row.item.ENGLISH_PHRASE" />
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
#diiv {
  max-height: 300px;
  margin-bottom: 2em;
}
</style>