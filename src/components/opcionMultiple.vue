<template>
  <div>
    <div v-for="(option, index) in $props.options">
      <b-form-group :label="option.pregunta" :id="index + ''" label-size="lg" label-class="labelPregunta">
        <b-form-radio-group               
          :name="index +''"
          :options="option.options"          
          stacked
          @change="dmensaje($event, index)"
        >         
        </b-form-radio-group>
      </b-form-group>      
    </div>
  </div>
</template>


<script>
export default {
  props: {
    options: Array,
    label: String,   
    rEsperadas: Array 
  },
  data() {
    return { 
      mensaje: "",
      Rrespuestas: []
    };
  },
  methods: {    
    enviar(checked) {      
      this.$emit('respuestas', checked);
    },
    verificacion: function(respuestas, rEsperadas) {         
      this.mensaje = "Preguntas incorrectas: ";      
      if (respuestas.length != rEsperadas.length) {
        this.mensaje = "DILIGENCIE TODAS LAS PREGUNTAS.";
      } else {
        for (var r = 0; r < respuestas.length; r++) {
          if (respuestas[r] != rEsperadas[r]) {
            this.mensaje = this.mensaje + (r + 1) + "-";
          }
        }
      }      
      if (this.mensaje == "Preguntas incorrectas: ") {
        this.mensaje = "PREGUNTAS CORRECTAS";
      }
      console.log(this.mensaje)
      this.enviar(this.mensaje)
    },
    dmensaje(valor, posicion){    
      this.Rrespuestas[posicion] = valor; 
      this.verificacion(this.Rrespuestas, this.rEsperadas)        
    }
  },
};
</script>

<style scoped>

/deep/.labelPregunta{
  font-weight: bold;
}

</style>