<template>
  <div>
    <div v-if="!tabla.camposInput">
      <b-table
        id="tabla"
        small
        :fields="tabla.fields"
        :items="tabla.items"
        responsive="sm"
        :bordered="tabla.bordered"
      >
        <!-- A virtual column -->
        <template v-slot:cell(#)="data">{{ data.index + 1 }}</template>
        <template v-slot:cell(html)="data">
          <h3 v-html="data.value"></h3>
        </template>
        
        <template v-slot:cell(html1)="data">
          <h3 v-html="data.value"></h3>
        </template>
        
        <template v-slot:cell(html2)="data">
          <h3 v-html="data.value"></h3>
        </template>


        <template v-slot:cell(html3)="data">
          <h3 v-html="data.value"></h3>
        </template>

        <template v-slot:cell(html4)="data">
          <h3 v-html="data.value"></h3>
        </template>


        <!-- A custom formatted column -->
        <template v-if="$props.tabla.camposInput" v-slot:cell(items)="row" id="hola">
          <inputChecked :resuelto="$props.inglesR" :esperado="row.item.ENGLISH_PHRASE" />
        </template>
      </b-table>
    </div>
    <div v-if="tabla.camposInput" class="overflow-auto" id="tablaInputs">     
      <b-table
        small
        :fields="tabla.fields"  
        :items="['ey']"      
        responsive="sm"
        :bordered="tabla.bordered"
      >
         
        <template v-slot:cell(Z)="row" :id="tabla.refs">        
          <posiblesRespuestasTabla :refs="$props.tabla.refs" :listadoPalabrasEsperadas="$props.tabla.items" :enlistada="tabla.enlistada" />
        </template>
        
      </b-table>      
      
    </div>    
  </div>
</template>

<script>
import inputChecked from "./inputChecked";
import posiblesRespuestasTabla from "./posiblesRespuestasTabla";
export default {
  components: {
    inputChecked,
    posiblesRespuestasTabla
  },
  data() {
    return {};
  },
  props: {
    tabla: Object,
  },
  mounted(){    
  }
};
</script>

<style scoped>
#tablaInputs {
  max-height: 350px;
  margin-bottom: 2em;
}
</style>