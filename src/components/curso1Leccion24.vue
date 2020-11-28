<template>
  <div>
    <div class="row">
      <h3 id="subTitulo">
        OTROS SUJETOS EN INGLÉS CONSIDERADOS TERCERA PERSONA (SHE- HE-IT)
      </h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <p class="parrafo">
          Todo subjeto singular que se refiera a una persona, cosa o animal es
          considerado como SHE, HE o It.
        </p>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <b-card>
          <listaIndex :tabla="$data.tablaP94" />
        </b-card>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <b-card>
          <listaIndex :tabla="$data.tablaP94P2" />
        </b-card>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <tablaTC
          id="diiv"
          class="overflow-auto"
          :cuestionario="$data.cuestionario2"
          :inglesR="false"
          :espanolR="false"
        />
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">PRACTICE</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <h5 style="text-align: justify">
          Completa las siguientes oraciones con alguno de estos nombres:
        </h5>
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <listaIndex :tabla="$data.tablaP95" />
      </div>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-6" id="text">
        <opcionMultiple
          :options="$data.cuestionarioP95"
          :rEsperadas="$data.respuestasCuestionarioP95"
          @respuestas="$data.mensajeRespuestasP95 = $event"
        />
      </div>
      <b-modal ref="my-modalP95" hide-footer title="RESULTADO">{{
        mensajeRespuestasP95
      }}</b-modal>
      <div class="col-sm-1"></div>
    </div>
    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-3">
        <b-button variant="primary" @click="showModal('my-modalP95')"
          >VERIFICAR PREGUNTAS</b-button
        >
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">EL USO DE ONE Y A- AN</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <p class="parrafo">
          En ingles la palabra “one” que literalmente significa “uno” como
          número puede ser usada en varios contextos. - Cuando se refiere al
          género del sujeto puede ser masculino, femenino o neutro:
        </p>
        <h3 class="colorLetraAzul">Un,una, o uno</h3>
        <ul>
          <li>
            <p class="parrafo">
              I have
              <span class="colorLetraRojo">one</span> brother
            </p>
          </li>
          <li>
            <p class="parrafo">
              I have
              <span class="colorLetraRojo">one</span> sister
            </p>
          </li>
          <li>
            <p class="parrafo">
              He is
              <span class="colorLetraRojo">one</span> of my brothers
            </p>
          </li>
        </ul>
        <p class="parrafo">
          Además, en inglés la palabra ONE sirve para reemplazar un sujeto del
          que ya hemos mencionado para no repetir la palabra. Veamos un ejemplo:
        </p>
        <ul>
          <li>
            <p class="parrafo">
              Esta
              <span class="colorLetraRojo">casa</span> cuesta $ 200.000 dólares,
              pero esta <span class="colorLetraRojo">casa</span> cuesta $
              250.000 dólares. this
              <span class="colorLetraRojo">house</span> costs $200.000 dollars
              but that <span class="colorLetraRojo">one</span> costs $250.000
              dollars
            </p>
            <h3>
              en este caso ONE significa “casa” porque es de lo estamos hablando
            </h3>
          </li>
        </ul>
        <p class="parrafo">
          En inglés también podemos usar la palabra
          <strong class="colorLetraAzul">a</strong> que se refiere a
          <span class="colorLetraAzul">Un- Una</span>
          <ul>
            <li>
              <h3>
                He is
                <span class="colorLetraRojo">a</span> teacher
                <li>
                  She is
                  <span class="colorLetraRojo">a</span> teacher
                </li>
              </h3>
            </li>
        
          </ul>
        </p>
        <p class="parrafo">
          Cuando la palabra empieza por vocal o suena como vocal usamos
          <span class="colorLetraAzul">an</span>
          <ul>
            <li>
              <h3>
                I have
                <span class="colorLetraRojo">an</span>apple
              </h3>
            </li>
            <li>
              <h3>
                I was
                <span class="colorLetraRojo">an</span>elephantr
              </h3>
            </li>
          </ul>
        </p>
        <p class="parrafo">
          Cuando se refiere al sujeto reflexivo es decir a
          <ul>
            <li>
              <h3>
                <span class="colorLetraRojo">One</span> never knows: uno nunca
                sabe
              </h3>
            </li>
          </ul>
        </p>
      </div>
    </div>

    <div class="row">
      <h3 id="subTitulo">PRACTICE</h3>
    </div>

    <div class="row">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <p class="parrafo">
          Complete con
          <strong>one (1), a o an.</strong> En algunas oraciones
          <strong>a</strong>
          o
          <strong>one (1)</strong> es posible
        </p>
      </div>
    </div>

    <div class="row" v-for="(item, index) in preguntasCompletarP93.items">
      <div class="col-sm-1"></div>
      <div class="col-sm-10">
        <div class="col-sm-1">
          <inputChecked
            :esperado="item.esperado"
            :name="preguntasCompletarP93.nombre + index"
            :conTexto="true"
            :textoA="item.textoA"
            :textoD="item.textoD"
            :tamano="item.tamano"
          />
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import posiblesRespuestasTabla from "./posiblesRespuestasTabla";
import opcionMultiple from "./opcionMultiple";
import listaIndex from "./listaIndex";
import inputChecked from "./inputChecked";
import tablaTC from "./tablaTraduccionCodigos";
export default {
  methods: {
    showModal(text) {
      this.$refs[text].show();
    },
  },
  components: {
    listaIndex,
    inputChecked,
    tablaTC,
    opcionMultiple,
  },
  data() {
    return {
      preguntasCompletarP93: {
        nombre: "preguntasCompletarP24",
        items: [
          {
            esperado: ["one"],
            textoA: "1. When I was a kid, I could count the numbers from",
            textoD: "to ten.",
            tamano: 44,
          },
          {
            esperado: ["One"],
            textoA: "2. ",
            textoD: "shouldn’t criticize someone we don’t know very well.",
            tamano: 42,
          },
          {
            esperado: ["an"],
            textoA: "3. I always eat",
            textoD: "apple for my breakfast.",
            tamano: 31,
          },
          {
            esperado: ["one"],
            textoA: "4. There is",
            textoD: "thing I don’t like about traveling for so long.",
            tamano: 41,
          },
          {
            esperado: ["one"],
            textoA: "5. I didn’t buy the red car. I bought the blue",
            textoD: ".",
            tamano: 35,
          },
          {
            esperado: ["one"],
            textoA: "6. ",
            textoD:
              "of my favorite songs is “the man in the mirror” by Michael Jackson.",
            tamano: 49,
          },
          {
            esperado: ["one"],
            textoA: "7. The probability to survive in the ocean is",
            textoD: "in a million.",
            tamano: 41,
          },
        ],
      },
      mensajeRespuestasP95: "Complete las preguntas",
      respuestasCuestionarioP95: [
        "B",
        "B",
        "C",
        "B",
        "A",
        "B",
        "A",
        "C",
        "B",
        "A",
      ],
      cuestionarioP95: [
        {
          respuesta: "",
          pregunta:
            "1. I didn’t go to the meeting because ____________ told me",
          options: [
            {
              text: "A) Nobody",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Everyone",
              value: "B",
              disabled: false,
            },
            {
              text: "C) That one",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "2. Police think I am crazy but I swear I saw _________ walking into the room.",
          options: [
            {
              text: "A) Very much",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Somebody",
              value: "B",
              disabled: false,
            },
            {
              text: "C) She",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "3. I can’t help you now but I´ll call _____________who can help you for sure.",
          options: [
            {
              text: "A) Nobody",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Nothing",
              value: "B",
              disabled: false,
            },
            {
              text: "C) A friend of mine",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "4. What did you buy at the store? _______ because I didn’t have money with me.",
          options: [
            {
              text: "A) Nobody",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Nothing",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Somebody",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "5. There is _________ I have to talk to you about",
          options: [
            {
              text: "A) Something",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Everyone",
              value: "B",
              disabled: false,
            },
            {
              text: "C) That one",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "6. He is a very famous Hollywood actor. ________ knows him.",
          options: [
            {
              text: "A) Nobody",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Everyone",
              value: "B",
              disabled: false,
            },
            {
              text: "C) That one",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta:
            "7. Excuse me, can you pass me my book on the table? - _______ ",
          options: [
            {
              text: "A) This one",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Everyone",
              value: "B",
              disabled: false,
            },
            {
              text: "C) Nothing",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "8. Which one is your car? -________ over there",
          options: [
            {
              text: "A) Nobody",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Everyone",
              value: "B",
              disabled: false,
            },
            {
              text: "C) That one",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "9. He is a nice guy. _______ loves him.",
          options: [
            {
              text: "A) Nobody",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Everyone",
              value: "B",
              disabled: false,
            },
            {
              text: "C) That one",
              value: "C",
              disabled: false,
            },
          ],
        },
        {
          respuesta: "",
          pregunta: "10. He is still lost. _______ has seen him for a week.",
          options: [
            {
              text: "A) Nobody",
              value: "A",
              disabled: false,
            },
            {
              text: "B) Everyone",
              value: "B",
              disabled: false,
            },
            {
              text: "C) That one",
              value: "C",
              disabled: false,
            },
          ],
        },
      ],
      cuestionario2: {
        fields: [
          { key: "A", thClass: "Yelow" },
          { key: "B", thClass: "Red" },
          { key: "C", thClass: "Blue" },

          { key: "complejo1", label: "WRITE HERE IN ENGLISH" },
          { key: "español", label: "WRITE HERE IN SPANISH" },
        ],
        items: [
          {
            A: 4,
            B: 3,
            C: 2,
            complejo1: { lista: ["Somebody needs you"] },
            español: "Alguien te necesita",
          },
          {
            A: 1,
            B: 5,
            C: 1,
            complejo1: { lista: ["Nothing is going to happen"] },
            español: "Nada va a pasar",
          },
          {
            A: 7,
            B: 5,
            C: 1,
            complejo1: { lista: ["Something good is going to happen"] },
            español: "Algo bueno va a pasar",
          },
          {
            A: 6,
            B: 1,
            C: 6,
            complejo1: { lista: ["Nobody is going to come"] },
            español: "Nadie va a venir",
          },
          {
            A: 3,
            B: 1,
            C: 5,
            complejo1: { lista: ["This one is mine"] },
            español: "Este es mío",
          },
          {
            A: 5,
            B: 1,
            C: 6,
            complejo1: { lista: ["A friend of mine is going to come"] },
            español: "Un amigo mío va a venir",
          },
          {
            A: 1,
            B: 7,
            C: 7,
            complejo1: { lista: ["Nothing impresses me more than that"] },
            español: "Nada me impresiona más que eso",
          },
          {
            A: 2,
            B: 2,
            C: 4,
            complejo1: { lista: ["Everyone knows me"] },
            español: "Todo el mundo me conoce",
          },
          {
            A: 4,
            B: 6,
            C: 4,
            complejo1: { lista: ["Somebody saw me"] },
            español: "Alguien me vio",
          },
          {
            A: 4,
            B: 1,
            C: 6,
            complejo1: { lista: ["Somebody is going to come"] },
            español: "Alguien va a venir",
          },
          {
            A: 8,
            B: 1,
            C: 5,
            complejo1: { lista: ["That one is mine"] },
            español: "Aquel es mío",
          },
          {
            A: 2,
            B: 8,
            C: 2,
            complejo1: { lista: ["Everybody thinks of you"] },
            español: "Todo el mundo te piensa",
          },
          {
            A: 4,
            B: 4,
            C: 8,
            complejo1: { lista: ["Somebody has to do it"] },
            español: "Alguien tiene que hacerlo",
          },
        ],
      },
      tablaP94: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "ingles", label: "Inglés" },
          { key: "trad1", label: "Traducción" },
          { key: "html", label: "Inglés" },
          { key: "trad2", label: "Traducción" },
        ],
        items: [
          {
            ingles: "Nobody",
            trad1: "Nadie",
            html:
              "<h5>Nobody know<span class='colorLetraRojo2'>s</span> me</h5>",
            trad2: "Nadie me conoce",
          },
          {
            ingles: "Somebody",
            trad1: "Alguien",
            html:
              "<h5>Somebody need<span class='colorLetraRojo2'>s</span> you</h5>",
            trad2: "Alguien te necesita",
          },
          {
            ingles: "Something",
            trad1: "Algo",
            html: "<h5>Something good is going to happen</h5>",
            trad2: "Algo bueno va a pasar",
          },
          {
            ingles: "Everyone",
            trad1: "Todo el mundo",
            html:
              "<h5>Everyone speak<span class='colorLetraRojo2'>s</span> English</h5>",
            trad2: "Todo el mundo habla ingles",
          },
          {
            ingles: "Nothing",
            trad1: "Nada",
            html:
              "<h5>Nothing impress<span class='colorLetraRojo2'>es</span> me more than that</h5>",
            trad2: "Nada me impresiona más que eso",
          },
          {
            ingles: "Nobody",
            trad1: "Nadie",
            html: "<h5>Nobody knows me</h5>",
            trad2: "Nadie me conoce",
          },
          {
            ingles: "That one",
            trad1: "Aquel, aquella",
            html: "<h5>That one is mine</h5>",
            trad2: "Aquel es mío",
          },
          {
            ingles: "This one",
            trad1: "Este",
            html:
              "<h5>This one look<span class='colorLetraRojo2'>s</span> better</h5>",
            trad2: "Este luce mejor",
          },
          {
            ingles: "A friend of mine",
            trad1: "Un amigo mío",
            html: "<h5>A friend of mine gave me this</h5>",
            trad2: "Un amigo mío me dio esto",
          },
        ],
      },
      tablaP95: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "1", label: "Nobody" },
          { key: "2", label: "Somebody" },
          { key: "3", label: "Something" },
          { key: "4", label: "Everyone" },
          { key: "5", label: "Nothing" },
          { key: "6", label: "That one" },
          { key: "7", label: "This one" },
          { key: "8", label: "A friend of mine" },
        ],
        items: [
          {
            1: "Nadie",
            2: "Alguien",
            3: "Algo",
            4: "Todos",
            5: "Nada",
            6: "Aquél",
            7: "Este",
            8: "Un amigo mio",
          },
        ],
      },
      tablaP94P2: {
        bordered: true,
        camposInput: false,
        fields: [
          { key: "1", label: "", thClass: "Yelow" },
          { key: "2", label: "", thClass: "Red" },
          { key: "3", label: "", thClass: "Blue" },
        ],
        items: [
          {
            1: "1. Nothing",
            2: "1. Is",
            3: "1. Happen",
          },
          {
            1: "2. Everyone",
            2: "2. Knows",
            3: "2. You",
          },
          {
            1: "3. This one",
            2: "3. Needs",
            3: "3. Willing to help",
          },
          {
            1: "4. Somebody",
            2: "4. Has",
            3: "4. Me",
          },
          {
            1: "5. A friend of mine",
            2: "5. Is going to",
            3: "5. Mine",
          },
          {
            1: "6. Nobody",
            2: "6. Saw",
            3: "6. Going to come",
          },
          {
            1: "7. Something Good",
            2: "7. Impresses me",
            3: "7. More than that",
          },
          {
            1: "8. That one",
            2: "8. Thinks of",
            3: "8. To do it",
          },
        ],
      },
    };
  },
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

/deep/ .colorText {
  color: white;
}

/deep/ .Blue {
  background-color: #002060;
  color: white;
}
/deep/ .Red {
  background-color: crimson;
  color: white;
}
/deep/ .Yelow {
  background-color: #ffc000;
  color: white;
}
/deep/ .Green {
  background-color: chartreuse;
}
/deep/ .Blue2 {
  background-color: #00b0f0;
  color: white;
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
/deep/.colorLetraRojo2 {
  color: red;
}
/deep/.colorLetraAzul {
  color: blue;
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

#textoCompromiso {
  text-align: left;
  margin-bottom: 1em;
  font-size: 1.5em;
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
  font-size: 1.5em;
  color: black;
  font-family: "PT Sans";
  font-weight: bold;
  margin-bottom: auto;
}
#numeroMagico2 {
  background: greenyellow;
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
</style>
