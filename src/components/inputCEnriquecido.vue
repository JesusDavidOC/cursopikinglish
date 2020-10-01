<template>
  <div style="display: inline-flex">
    <div class="row">
      <div :class="'col-sm-' + object.tamano1">
        <inputChecked
          :esperado="object.lista1"
          :resuelto="false"
          :name="object.name"
          :conTexto="true"
          :textoA="object.textoA"
          :textoD="object.textoD"
        />
      </div>
    </div>
    <div :class="'col-sm-' + object.tamano2">
      <inputChecked
        :esperado="object.lista2"
        :resuelto="false"
        :name="object.name + '2'"
        :conTexto="true"
        textoA=""
        :textoD="object.textoD2"
      />
    </div>
  </div>
</template>

<script>
import inputChecked from "./inputChecked";
/**lista1: Array,
        lista2: Array,
        textoA: String,
        textoD: String,
        textoD2: String*/

export default {
  props: {
    object: Object,
  },
  components: {
    inputChecked,
  },
};
</script>>


<style scoped>
#here {
  padding: 0;
}
</style>



