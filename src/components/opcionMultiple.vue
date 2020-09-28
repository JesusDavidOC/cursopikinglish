<template>
  <div>
    <div
      v-for="(option, index) in $props.options"
      id="contenedorPregunta"
      class="row"
    >
      <div class="col-sm-8">
        <b-form-group
          :label="option.pregunta"
          :id="index + ''"
          label-size="lg"
          label-class="labelPregunta"
        >
          <b-form-radio-group
            :name="index + ''"
            :options="option.options"
            stacked
            @change="dmensaje($event, index)"
          >
          </b-form-radio-group>
        </b-form-group>
      </div>
      <div class="col-sm-2" style="padding:0;">
        <b-button        
          id="paraAudio"
          variant="primary"
          v-if="option.audio != undefined"
          class="btn btn-outline-secondary"
          type="button"
          @click.prevent="playSound(option.audio)"
        >
          <i class="fa fa-play"></i>
        </b-button>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  props: {
    options: Array,
    label: String,
    rEsperadas: Array,
  },
  data() {
    return {
      mensaje: "",
      Rrespuestas: [],
    };
  },
  methods: {
    playSound(sound) {
      if (sound) {
        var audio = new Audio(sound);
        audio.play();
      }
    },
    enviar(checked) {
      this.$emit("respuestas", checked);
    },
    verificacion: function (respuestas, rEsperadas) {
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
      console.log(this.mensaje);
      this.enviar(this.mensaje);
    },
    dmensaje(valor, posicion) {
      this.Rrespuestas[posicion] = valor;
      this.verificacion(this.Rrespuestas, this.rEsperadas);
    },
  },
};
</script>

<style scoped>
/deep/.labelPregunta {
  font-weight: bold;
}

#paraAudio {
  padding-left: 0.8em;
  padding-right: 0.7em;
  padding-top: 0.5em;
  padding-bottom: 0.5em;  
  border-radius: 2.5em;  
  color: white;
  border-color: white;
}
</style>