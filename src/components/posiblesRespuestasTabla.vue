<template>
  <div class="row">
    <div class="row" v-for="(item, index) in listadoPalabrasEsperadas">
      <inputChecked        
        :esperado="listadoPalabrasEsperadas"
        :resuelto="false"
        :name="refs+index+''"
        @output="dinamizadorPalabras(index)"
        :ref="$props.refs"
      />
    </div>
  </div>
</template>

<script>
import inputChecked from "./inputChecked";
export default {
  components: {
    inputChecked,
  },
  props: {
    listadoPalabrasEsperadas: Array,
    refs: String,
  },
  data() {
    return {
      listadoPalabrasEsperadas2: this.quitarMayusculas(
        this.listadoPalabrasEsperadas
      ),
    };
  },
  methods: {
    dinamizadorPalabras(index) {
      var estan = [];

      for (let j = 0; j < this.$refs[this.refs].length; j++) {
        estan.push(this.$refs[this.refs][j].$data.text);
      }
      
      var nuevo = this.listadoPalabrasEsperadas;
      for (let i = 0; i < estan.length; i++) {
        if (estan[i] != "") {
          nuevo = this.eliminarPalabra(estan[i], nuevo);
        }
      }      
      if (nuevo.length > 0) {
        for (let t = 0; t < this.$refs[this.refs].length; t++) {          
          if (
            this.quitarMayusculas(estan).includes(
              this.quitarAcentos(
                this.$refs[this.refs][t].$data.text
              ).toLowerCase()
            ) &&
            this.$refs[this.refs][t].$data.text != ""
          ) {        
            this.$refs[this.refs][t].$data.disab = false;     
          } else {
            this.$refs[this.refs][t].$data.esperado1 = nuevo;
          }
        }
      }
    },
    eliminarPalabra(palabra, arreglo) {
      palabra = this.quitarAcentos(palabra).toLowerCase();
      var nuevo = [];
      for (let index = 0; index < arreglo.length; index++) {
        const element = arreglo[index];
        if (palabra != element) {
          nuevo.push(element);
        }
      }
      // funcionaaaaaa si imprime a nuevo
      return nuevo;
    },
    quitarAcentos(cadena) {
      const acentos = {
        á: "a",
        é: "e",
        í: "i",
        ó: "o",
        ú: "u",
        Á: "A",
        É: "E",
        Í: "I",
        Ó: "O",
        Ú: "U",
      };
      return cadena
        .split("")
        .map((letra) => acentos[letra] || letra)
        .join("")
        .toString();
    },
    quitarMayusculas(arreglo) {
      for (let i = 0; i < arreglo.length; i++) {
        arreglo[i] = this.quitarAcentos(arreglo[i].toLowerCase());
      }
      return arreglo;
    },
  },
};
</script>

<style scoped>
</style>

