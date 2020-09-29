<template>
  <div>

      <div class="row">
        <div class="col-sm-12">
          <h3 id="subTitulo">PRACTICE</h3>
        </div>
      </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice">Elegir la palabra mas acorde a la oración. <strong>NEVER, ALREADY, EVER, YET AND JUST   </strong></a>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-11 row">
        <tablaTC :cuestionario="tablaP23" />
      </div>
    </div>

      <div class="row">
        <div class="col-sm-12">
          <h3 id="subTitulo">FORMA PROGRESIVA</h3>
        </div>
      </div>

    <div class="row">
      <div class="col-sm-2"></div>
      <div class="col-sm-8" id="cuadroTexto"> 
        <img src="https://classroom.pikinglish.com/cursos/curso1/leccion18/imagenes/imagen3.JPG" />
      </div>
      <div class="col-sm-2"></div>
    </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice"><strong>Is: Es-Esta</strong></a>
      </div>
    </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice"><strong>Am: Soy-Estoy</strong></a>
      </div>
    </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice"><strong>Are: Eres-Estás/Somos-Estamos/Son-Están</strong></a>
      </div>
    </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice"><strong>Was: Era-Estaba</strong></a>
      </div>
    </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice"><strong>Were: Eras-Estabas/ Éramos- Estábamos/Eran-Estaban</strong></a>
      </div>
    </div>

      <div class="row">
        <div class="col-sm-12">
          <h3 id="subTitulo">¿COMO AGREGAR “ING”?</h3>
        </div>
      </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-11 row">
        <tablaTC :cuestionario="tablaP33" />
      </div>
    </div>

      <div class="row">
        <div class="col-sm-12">
          <h3 id="subTitulo">PRACTICE</h3>
        </div>
      </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice"><i class="fa fa-diamond" style="font-size: 1.0em;"></i>Escriba el verbo con poder según la oración IS-AM-ARE-WAS-WERE y ponga unos
        de los siguientes verbos en su forma correcta de acuerdo a la oración.</a>
      </div>
    </div>

    <div class="row">
          <div class="col-sm-2"></div>
          <div class="col-ms-8">
              <h3><strong>Ask – rain – happen - talk - talk – say – drive – lie – do – listen-</strong></h3>
          </div>
          <div class="col-sm-2"></div>
    </div>
    <br>

    <div class="row" v-for="(item, index) in preguntasCompletarP24.items" :key="index">
      <div class="col-sm-1"></div>
      <div class="col-sm-8">
        <div :class="'col-sm-'+item.tamaño">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP24.nombre+index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
            :audio="item.audio"
          />
        </div>
      </div>
    </div>

      <div class="row">
        <div class="col-sm-12">
          <h3 id="subTitulo">SUPER POWER VERBS</h3>
        </div>
      </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id=textPractice><i class="fa fa-diamond" style="font-size: 1.0em;"></i>Existen unos verbos con súper poderes que <span class="colorLetraRojo">SE PUEDEN NEGAR, AFIRMAR Y PREGUNTAR, ES DECIR NO NECESITAN UN AUXILIAR</span></a>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <tablaTC :cuestionario="tablaP53" />
      </div>
      <div class="col-sm-1"></div>
    </div>

<div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10" style="text-align:left;">
        <a id="textPractice">Completar la tabla en inglés</a>
      </div>
    </div>

    <div class="row" id="tablas">
        <div class="col-sm-1"></div>
        <div class="col-sm-7" id="tabla">
            <tablaTC
              :cuestionario="$data.tablaZ1"
              :inglesR="false"
              :espanolR="false"
              />

        </div>
        <div class="col-sm-3" id="tabla">
            <tablaTC
            :cuestionario="$data.tablaV1"
            :inglesR="false"
            :espanolR="false"
            />
        </div>  
        <div class="col-sm-1"></div>
    </div>

    <div class="row">
      <div class="col-sm-2"></div>
          <div class="col-sm-8">
            <tablaTC
              :cuestionario="$data.tablaQ1"
              :inglesR="false"
              :espanolR="false"
              
            />
        </div>
      <div class="col-lg-2"></div>
    </div>

  </div>
</template>

<script>
    import listaIndex from "./listaIndex";
    import opcionMultiple from "./opcionMultiple";
    import inputChecked from "./inputChecked";
    import tablaTC from "./tablaTraduccionCodigos";

    export default {
        
    components: {
        listaIndex,
        tablaTC,
        opcionMultiple,
        inputChecked,
    },
    data(){
        return{

      tablaQ1: {
        fields: [
          { key: "complejo1", label: " Pronuciacion" },
        ],
        items: [
          {
            complejo1: { lista: ["Have, Has, Had, Am, Is, Are, Was, Were, Should, Could, Can, Must ","Have Has Had Am Is Are Was Were Should Could Can Must"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion18/audios/page%2075/AC1P75R1superpowerverbs.mp3"},
          },
          {
            complejo1: { lista: ["Haven ́t, Hasn ́t, Hadn ́t, Am not, Isn ́t, Aren ́t, Wasn ́t, Weren ́t, Shouldn ́t, Couldn ́t, Can ́t, Mustn ́t","Haven ́t Hasn ́t Hadn ́t Am not Isn ́t Aren ́t Wasn ́t Weren ́t Shouldn ́t Couldn ́t Can ́t Mustn ́t"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion18/audios/page%2075/AC1P75R2negation.mp3" },
          },
        ],
      },

      tablaZ1: {
        fields: [
          { key: "Traducción" },
          { key: "complejo1", label: " Super Power Verb" },
        ],
        items: [
          {
            Traducción: "Haber, he, has, hemos, han",
            complejo1: { lista: ["Have"]},
          },
          {
            Traducción: "Ha",
            complejo1: { lista: ["has"] },
          },
          {
            Traducción: "Había",
            complejo1: { lista: ["had"] },
          },
          {
            Traducción: "Soy-estoy",
            complejo1: { lista: ["am"] },
          },
          {
            Traducción: "Es-esta",
            complejo1: { lista: ["is"] },
          },
          {
            Traducción: "Eres-estás, somos-estamos, son y están.",
            complejo1: { lista: [" are"] },
          },
          {
            Traducción: "Era-estaba",
            complejo1: { lista: ["was"] },
          },
          {
            Traducción: "Eras-estabas, éramos/estábamos, eran y estaban",
            complejo1: { lista: ["were"] },
          },
          {
            Traducción: "Debería",
            complejo1: { lista: ["Should"] },
          },
          {
            Traducción: "Pude, podía y podría",
            complejo1: { lista: ["could"] },
          },
          {
            Traducción: "Poder",
            complejo1: { lista: ["can"]},
          },
          {
            Traducción: "Deber",
            complejo1: { lista: ["must"] },
          },
        ],
      },

      tablaV1: {
        fields: [
          { key: "complejo1", label: "“T Sound“" },
        ],
        items: [
          {complejo1: { lista: ["Participle"] }},
          {complejo1: { lista: ["Participle"] }},
          {complejo1: { lista: ["Participle"] }},
          {complejo1: { lista: ["Progressive"] }},
          {complejo1: { lista: ["Progressive"] }},
          {complejo1: { lista: ["Progressive"] }},
          {complejo1: { lista: ["Progressive"] }},
          {complejo1: { lista: ["Progressive"] }},
          {complejo1: { lista: ["Present"] }},
          {complejo1: { lista: ["Present"] }},
          {complejo1: { lista: ["Present"] }},
          {complejo1: { lista: ["Present"] }},
        ],
      },

        tablaP53: {
            fields: [

            { key: "su", label:"SUPER POWER VERB" },
            { key: "tr", label:"Traducción"},
            { key: "ne", label:"Negación"  },
            ],
            items: [
            {
                su: "Have",
                tr: "Haber, he, has, hemos, han",
                ne: "Haven´t",
            },
            {
                su: "Has",
                tr: "Ha",
                ne: "Hasn´t",
            },
            {
                su: "Had",
                tr: "Había",
                ne: "Hadn´t",
            },
            {
                su: "Am",
                tr: "Soy-estoy",
                ne: "Am not",
            },
            {
                su: "Is",
                tr: "Es-esta",
                ne: "Isn´t",
            },
            {
                su: "Are",
                tr: "Eres-estás, somos-estamos, son y están.",
                ne: "Aren´t",
            },
            {
                su: "Was",
                tr: "Era-estaba",
                ne: "Wasn´t",
            },
            {
                su: "Were",
                tr: "Eras-estabas, éramos/estábamos, eran y estaban",
                ne: "Weren´t",
            },
            {
                su: "Should",
                tr: "Debería",
                ne: "Shouldn´t",
            },
            {
                su: "Could",
                tr: "Pude, podía y podría",
                ne: "Couldn´t",
            },
            {
                su: "Can",
                tr: "Poder",
                ne: "Can´t",
            },
            {
                su: "Must",
                tr: "Deber",
                ne: "Mustn´t",
            },
            ],
          },

      preguntasCompletarP24: {
        nombre: "preguntasCompletarP24",
        items: [
          {
            esperado: ["are not talking"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion18/audios/page%2074/AC1P74R1.mp3",
            textoA: "1. We",
            textoD: "to you. (No estamos hablando contigo)",
            tamaño: 9,
          },
          {
            esperado: ["is not raining"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion18/audios/page%2074/AC1P74R2.mp3",
            textoA: "2. It",
            textoD: ". (No está lloviendo)",
            tamaño: 7,
          },
          {
            esperado: ["was she doing"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion18/audios/page%2074/AC1P74R3.mp3",
            textoA: "3. What",
            textoD: "there? (¿Qué estaba ella haciendo allá?))",
            tamaño: 10,
          },
          {
            esperado: ["are"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion18/audios/page%2074/AC1P74R4.mp3",
            textoA: "4. Who",
            textoD: "they? (¿Quiénes son ellos?)",
            tamaño: 7,
          },
          {
            esperado: ["am saying"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion18/audios/page%2074/AC1P74R5.mp3",
            textoA: "5. Do you understand what I",
            textoD: "(¿Entiendes lo que estoy diciendo?)",
            tamaño: 12,
          },
          {
            esperado: ["was driving"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion18/audios/page%2074/AC1P74R6.mp3",
            textoA: "6. I",
            textoD: "home from work (Estaba conduciendo a casa del trabajo)",
            tamaño: 11,
          },
          {
            esperado: ["asking"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion18/audios/page%2074/AC1P74R7.mp3",
            textoA: "7. There is someone at the door",
            textoD: "for you. (Hay alguien en la puerta preguntando por ti)",
            tamaño:8  ,
          },
          {
            esperado: ["are you liying"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion18/audios/page%2074/AC1P74R8.mp3",
            textoA: "8. Why",
            textoD: "to me? (¿Por qué estás mintiéndome?)",
            tamaño: 10,
          },
          {
            esperado: ["were you talking"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion18/audios/page%2074/AC1P74R9.mp3",
            textoA: "9. Who",
            textoD: "to? (¿Con quién estabas hablando?)",
            tamaño: 10,
          },
          {
            esperado: ["is happening"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion18/audios/page%2074/AC1P74R10.mp3",
            textoA: "10. What",
            textoD: "here? (¿Qué está pasando aquí?)",
            tamaño: 9,
          },
          {
            esperado: ["were listening"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion18/audios/page%2074/AC1P74R11.mp3",
            textoA: "11. They",
            textoD: "to music (Ellos estaban escuchando música)",
            tamaño: 11,
          },
          {
            esperado: ["was"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion18/audios/page%2074/AC1P74R12.mp3",
            textoA: "12. She",
            textoD: "not at home (Ella no estaba en casa)",
            tamaño: 8,
          },
          {
            esperado: ["are"],audio:"https://classroom.pikinglish.com/cursos/curso1/leccion18/audios/page%2074/AC1P74R13.mp3",
            textoA: "13. What ",
            textoD: "their names? (¿Cuáles son sus nombres?)",
            tamaño: 9,
          },
        ],
      },

        tablaP33: {
            fields: [

            { key: "TERMINO" },
            { key: "EXPLICACION"},
            { key: "PALABRAS",  },
            ],
            items: [
            {
                TERMINO: "Los que terminan en “e”",
                EXPLICACION: "Se omite la “e” y se agrega ING",
                PALABRAS: "Love-Loving",
            },
            {
                TERMINO: "Los que tienen una sola silaba",
                EXPLICACION: "Se duplica la última consonante y agrega ING",
                PALABRAS: "Plan-Planning",
            },
            {
                TERMINO: "Los que termina en “ie”",
                EXPLICACION: "Se omite “ie” y se cambia por “Y” más ING",
                PALABRAS: "Lie-Lying",
            },
            {
                TERMINO: "Los demás verbos",
                EXPLICACION: "Se les agrega ING",
                PALABRAS: "Work-Working",
            },
            ],
          },

        tablaP23: {
            fields: [

            { key: "FRASES", thClass: "Yelow" },
            { key: "complejo1", label: "PHARES", thClass: "Yelow" },
            ],
            items: [
            {
                FRASES: "1. Yo acabo de dejar el paquete en tu casa",
                complejo1: {
                lista: ["just"],
                textoA: "I have",
                textoD: "dropped the package at your house.",
                tamano: 33,
                },
            },
            {
                FRASES: "2. Aún no le he preguntado a él",
                complejo1: {
                lista: ["yet"],
                textoA: "I have not asked him",
                textoD: "",
                tamano: 21,
                },
            },
            {
                FRASES: "3. Yo acabo de terminar de cocinar",
                complejo1: {
                lista: ["just"],
                textoA: "I have",
                textoD: "finished cooking",
                tamano: 22,
                },
            },
            {
                FRASES: "4. ¿Has visto alguna vez la nieve?",
                complejo1: {
                lista: ["ever"],
                textoA: "Have you",
                textoD: "seen snow?",
                tamano: 23,
                },
            },
            {
                FRASES: "5. Él aún no ha saltado",
                complejo1: {
                lista: ["yet"],
                textoA: "He has not jumped",
                textoD: "",
                tamano: 21,
                },
            },
            {
                FRASES: "6. Él nunca ha patinado sobre hielo",
                complejo1: {
                lista: ["never"],
                textoA: "He has",
                textoD: "ice-skated",
                tamano: 20,
                },
            },
            {
                FRASES: "7. Él acaba de llamarla",
                complejo1: {
                lista: ["just"],
                textoA: "He has",
                textoD: "called her",
                tamano: 20,
                },
            },
            {
                FRASES: "8. ¿Ella ya te ha enviado el correo?",
                complejo1: {
                lista: ["yet"],
                textoA: "Has she sent you the email",
                textoD: "?",
                tamano: 25,
                },
            },
            {
                FRASES: "9. Él ya ha hecho eso",
                complejo1: {
                lista: ["already"],
                textoA: "He has",
                textoD: "done that",
                tamano: 21,
                },
            },
            {
                FRASES: "10.¿Ha ella alguna vez estado en Grecia?",
                complejo1: {
                lista: ["ever"],
                textoA: "Has she",
                textoD: "been to Greece",
                tamano: 23,
                },
            },
            ],
          },

        }
    }
};
</script>

<style scoped>
#textPractice {
  text-align: left;
  margin-bottom: 1em;
  font-size: 1.5em;
}
/deep/.labelPregunta {
  font-weight: bold;
}

/deep/ #tabla {
  padding-right: 0px;
  padding-left: 0px;
}
/deep/ .row {
  width: 100%;
  margin: 0;
  margin-bottom: 1em;
  padding: 0;
}

/deep/ #EnglishInput,
#SpanishInput {
  width: 100%;
}

/deep/ .Blue {
  background-color: cornflowerblue;
}
/deep/ .Blue2 {
  background-color: rgb(154, 189, 253);
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

/deep/.colorLetraRojo {
  color: red;
  margin-left: 8px;
  margin-right: 8px;
}

#cuadroTexto {
  margin-bottom: 1em;
}

img {
  width: 100%;
}

/deep/ #textRequired {
  width: 200px;
}

/deep/ #inputText {
  margin: 0;
  display: inline-flex;
}

#titulo {
  color: red;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 1.5em;
}

#subTitulo {
  padding: 0;
  margin-right: auto;
  color: darkcyan;
  margin-top: 1.5em;
  text-align: left;
}
.textList {
  font-size: 1.5em;
}

#numeroMagico2,
#numeroMagico4,
#numeroMagico5,
#numeroMagico12 {
  background-color: salmon;
  margin-right: auto;
  margin-left: auto;
  padding-top: 0.5em;
  padding-bottom: 0.5em;
  border-style: solid;
  border-radius: 1em;
  border-color: black;
  font-size: 2em;
  color: black;
  font-family: "PT Sans";
  font-weight: bold;
  margin-bottom: auto;
}
#numeroMagico2 {
  background: yellow;
}

#numeroMagico4 {
  background: red;
}
#numeroMagico5 {
  background: royalblue;
}
#numeroMagico12 {
  background: cadetblue;
}

#text,
#inputText {
  text-align: left;
  margin-left: 1em;
}

#textoCompromiso {
  text-align: left;
  margin-bottom: 1em;
  font-size: 1.5em;
}
#i {
  padding-right: 0;
  text-align: end;
}
</style>