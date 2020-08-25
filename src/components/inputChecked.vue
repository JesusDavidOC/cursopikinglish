<template>
  <div class="input-group">
    <b-form-input
      :name="this.name"
      :id="this.name+esperado[0]"
      v-model="text"
      :state="this.contiene()"      
      aria-describedby="input-live-help input-live-feedback"
      trim
    ></b-form-input>
    <div class="input-group-append">
      <button class="btn btn-outline-secondary" type="button" v-on:click="completar">
        <i class="fa fa-eye"></i>
      </button>
    </div>
  </div>
</template>


<script>
export default {
  props: {
    esperado: Array,
    resuelto: Boolean,
    name: "",   
  },
  data() {
    return {
      text: "",
      esperado1: this.esperado,
    };
  },
  methods: {
    completar() {
      this.text = this.esperado1[0];
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
    contiene() {
      //console.log(this.esperado1)
      this.text = this.text.replace("´", "'");
      if (this.esperado1.includes(this.quitarAcentos(this.text.toLowerCase()))) {        
        this.$emit("output", this.text);
        return true;
      }
      return false;
    },
  },
  mounted() {
    if (this.resuelto) {
      this.text = this.esperado1[0];
    }
  },
};
</script>

<style scoped>
.input-group-append {
  height: 100%;
}
</style>