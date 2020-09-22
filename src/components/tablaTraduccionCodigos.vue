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
        <div v-if="row.item.complejo1.tamano !=0" >
        <inputChecked :style="'width:'+row.item.complejo1.tamano+'em;'"
          :resuelto="$props.inglesR"
          :esperado="row.item.complejo1.lista"
          :conTexto="true"
          :textoA="row.item.complejo1.textoA"
          :textoD="row.item.complejo1.textoD"
<<<<<<< HEAD
          
          
=======
          :audio="row.item.complejo1.audio"
>>>>>>> 0944ae4927047063fa344f475a585a99866687f6
        />
        </div>
      </template>
      <template v-slot:cell(complejo2)="row" id="hola">
        
        <inputChecked :style="'width:'+row.item.complejo2.tamano+'em;'"
          :resuelto="$props.inglesR"
          :esperado="row.item.complejo2.lista"
          :conTexto="true"
          :textoA="row.item.complejo2.textoA"
          :textoD="row.item.complejo2.textoD"
           :audio="row.item.complejo2.audio"
        />
      </template>

      <template v-slot:cell(complejo3)="row" id="hola">
        <inputChecked :style="'width:'+row.item.complejo3.tamano+'em;'"
          :resuelto="$props.inglesR"
          :esperado="row.item.complejo3.lista"
          :conTexto="true"
          :textoA="row.item.complejo3.textoA"
          :textoD="row.item.complejo3.textoD"
           :audio="row.item.complejo3.audio"
        />
      </template>

      <template v-slot:cell(complejo4)="row" id="hola">
        <inputChecked :style="'width:'+row.item.complejo4.tamano+'em;'"
          :resuelto="$props.inglesR"
          :esperado="row.item.complejo4.lista"
          :conTexto="true"
          :textoA="row.item.complejo4.textoA"
          :textoD="row.item.complejo4.textoD"
           :audio="row.item.complejo4.audio"
        />
      </template>
      
      <template v-slot:cell(complejo5)="row" id="hola">
        <inputChecked :style="'width:'+row.item.complejo5.tamano+'em;'"
          :resuelto="$props.inglesR"
          :esperado="row.item.complejo5.lista"
          :conTexto="true"
          :textoA="row.item.complejo5.textoA"
          :textoD="row.item.complejo5.textoD"
           :audio="row.item.complejo5.audio"
        />
      </template>      

      <template v-slot:cell(TRADUCCION_ESPAÑOL)="row">
        <inputChecked :resuelto="$props.espanolR" :esperado="row.item.TRADUCCION_ESPAÑOL" />
      </template>
       <template v-slot:cell(html1)="row" id="hola">
        <a v-html="row.item.html1"> {{ row.item.html1 }} </a>
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